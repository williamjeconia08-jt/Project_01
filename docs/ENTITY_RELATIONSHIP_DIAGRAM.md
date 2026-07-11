# SmartCent Entity Relationship Diagram (ERD)

**Document Version:** 1.0

**Project:** SmartCent

**Phase:** System Design

**Status:** Draft

---

# 1. Purpose

This document defines the relationships between the entities in the SmartCent database.

It provides two complementary views:

1. Domain ERD (Business View)
2. Physical ERD (Database View)

Together, these diagrams provide both a high-level understanding of the system and the detailed relationships required for implementation.

---

# 2. Why Two ERDs?

As SmartCent grows, a single ERD containing every table becomes difficult to read.

To improve clarity, the architecture is divided into:

- Domain ERD – focuses on business domains and their interactions.
- Physical ERD – focuses on database tables, keys, and cardinality.

This approach is commonly used in enterprise software projects.

---

# 3. Domain ERD (Business View)

```

```
                     SmartCent

                          │

        ┌─────────────────┼─────────────────┐

        ▼                 ▼                 ▼

 Authentication      Learning         Gamification

        │                 │                 │

        ▼                 ▼                 ▼

 User/Profile     Course → Module → Lesson  XP/Badges

        │                 │                 │

        ├──────────────┐  ▼                 │

        ▼              │ Quiz Engine        │

     Wallet            │                    │

        ▼              ▼                    ▼

   Budgeting     Quiz Attempts       Achievements

        │                                   │

        └──────────────┬────────────────────┘

                       ▼

                 Challenges

                       │

                       ▼

                 Notifications

                       │

                       ▼

                 AI Recommendations

```

```

---

# 4. Domain Responsibilities

## Authentication

Responsible for:

- User accounts
- Login
- Registration
- Password reset
- Session management

---

## Learning

Responsible for:

- Courses
- Modules
- Lessons
- Educational content

---

## Quiz Engine

Responsible for:

- Questions
- Answers
- Quiz attempts
- Scoring

---

## Wallet

Responsible for:

- Virtual currency
- Rewards
- Spending
- Transactions

---

## Budgeting

Responsible for:

- Budgets
- Spending categories

---

## Savings

Responsible for:

- Savings goals
- Contributions

---

## Gamification

Responsible for:

- XP
- Levels
- Badges
- Achievements

---

## Challenges

Responsible for:

- Daily challenges
- Weekly challenges
- Streaks

---

## Notifications

Responsible for:

- User alerts
- Reward notifications
- Reminders

---

## AI

Responsible for:

- Personalized recommendations
- Learning paths
- Future adaptive learning

---

# 5. Physical ERD (Database View)

The following sections describe the relationships between individual entities.

---

## Authentication

User

1 ─────── 1 UserProfile

1 ─────── N RefreshToken

1 ─────── N PasswordResetToken

1 ─────── 1 Wallet

1 ─────── 1 UserPreference

---

## Learning

Course

1

↓

N Module

Module

1

↓

N Lesson

Lesson

1

↓

N LessonContent

Lesson

1

↓

N Quiz

Quiz

1

↓

N Question

Question

1

↓

N AnswerOption

---

## Quiz Engine

User

1

↓

N QuizAttempt

Quiz

1

↓

N QuizAttempt

QuizAttempt

1

↓

N QuizAnswer

Question

1

↓

N QuizAnswer

AnswerOption

1

↓

N QuizAnswer

---

## Wallet

Wallet

1

↓

N WalletTransaction

---

## Budgeting

User

1

↓

N Budget

Budget

1

↓

N BudgetCategory

---

## Savings

User

1

↓

N SavingsGoal

SavingsGoal

1

↓

N GoalContribution

---

## Gamification

Level

1

↓

N User

User

1

↓

N XPTransaction

Badge

N

↕

N User

Implemented through:

UserBadge

Achievement

N

↕

N User

Implemented through:

UserAchievement

---

## Challenges

Challenge

N

↕

N User

Implemented through:

UserChallenge

User

1

↓

1 DailyStreak

---

## Notifications

User

1

↓

N Notification

---

## AI

User

1

↓

N AIRecommendation

LearningPath

1

↓

N AIRecommendation

---

## Administration

User

1

↓

N Feedback

User

1

↓

N AuditLog

AppSetting

Independent reference entity.

---

# 6. Cardinality Summary

| Relationship | Cardinality |
|--------------|-------------|
| User → UserProfile | 1 : 1 |
| User → Wallet | 1 : 1 |
| User → Preferences | 1 : 1 |
| Course → Module | 1 : N |
| Module → Lesson | 1 : N |
| Lesson → Quiz | 1 : N |
| Quiz → Question | 1 : N |
| Question → AnswerOption | 1 : N |
| User → QuizAttempt | 1 : N |
| QuizAttempt → QuizAnswer | 1 : N |
| Wallet → WalletTransaction | 1 : N |
| User → Budget | 1 : N |
| Budget → BudgetCategory | 1 : N |
| User → SavingsGoal | 1 : N |
| SavingsGoal → GoalContribution | 1 : N |
| User ↔ Badge | M : N |
| User ↔ Achievement | M : N |
| User ↔ Challenge | M : N |
| User → Notification | 1 : N |
| User → AIRecommendation | 1 : N |

---

# 7. Junction Tables

The following tables exist solely to resolve many-to-many relationships:

| Junction Table | Connects |
|----------------|----------|
| UserBadge | User ↔ Badge |
| UserAchievement | User ↔ Achievement |
| UserChallenge | User ↔ Challenge |

These tables may also store metadata such as:

- earned_at
- completed_at
- progress
- status

---

# 8. Design Decisions

- UUIDs are used as primary keys for all entities.
- Foreign keys enforce referential integrity.
- Junction tables resolve many-to-many relationships.
- Audit fields (`created_at`, `updated_at`) are included on business entities.
- Soft deletes (`deleted_at`) are used where historical data should be retained.
- Transactional tables are immutable after creation unless business rules require updates.

---

# 9. Next Steps

With the logical relationships defined, the next stage is API design.

The API Design document will map business operations to REST endpoints, define request and response models, authentication flows, versioning strategy, and error handling conventions.

This ensures that every API endpoint is built directly on top of the validated database model established in the previous documents.