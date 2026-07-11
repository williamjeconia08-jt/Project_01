# SmartCent Entity Specifications

**Version:** 1.0

**Phase:** System Design

**Status:** Draft

---

# 1. Purpose

This document provides the complete specification for every database entity within SmartCent.

For each entity it defines:

- Purpose
- Category
- Attributes
- Data Types
- Constraints
- Relationships
- Business Rules
- Example Record

This document acts as the bridge between the logical database design and the physical PostgreSQL implementation.

---

# 2. Entity Categories

SmartCent classifies entities into four architectural categories.

---

## Core Entities

Core entities represent the primary business objects.

Examples:

- User
- Course
- Lesson
- Wallet

Characteristics:

- Long lifespan
- Frequently referenced
- Usually own other records

---

## Transactional Entities

Transactional entities record actions performed by users.

Examples:

- QuizAttempt
- WalletTransaction
- XPTransaction

Characteristics:

- Grow rapidly
- Time-based
- Never edited after creation

---

## Junction Entities

Used to resolve many-to-many relationships.

Examples:

- UserBadge
- UserAchievement
- UserChallenge

Characteristics:

- Mostly foreign keys
- Lightweight
- Connect two business entities

---

## Reference Entities

Reference entities contain relatively static data.

Examples:

- Badge
- Level
- BudgetCategory

Characteristics:

- Rarely modified
- Frequently read
- Shared across the application

---

# 3. Entity Template

Every entity follows this specification.

## Entity Name

### Category

(Core / Transactional / Junction / Reference)

### Purpose

Why the entity exists.

### Attributes

| Column | Type | Constraints | Description |

### Relationships

Incoming and outgoing relationships.

### Business Rules

Rules enforced by the application.

### Example Record

Example JSON object.

---

# 4. Entity Specifications

---

# 4.1 User

## Category

Core Entity

### Purpose

Represents a registered SmartCent user.

### Attributes

| Column | Type | Constraints | Description |
|--------|------|-------------|-------------|
| id | UUID | PK | User identifier |
| email | VARCHAR(255) | UNIQUE, NOT NULL | Login email |
| password_hash | TEXT | NOT NULL | Encrypted password |
| username | VARCHAR(50) | UNIQUE | Display username |
| role | VARCHAR(20) | DEFAULT 'student' | User role |
| is_verified | BOOLEAN | DEFAULT FALSE | Email verified |
| is_active | BOOLEAN | DEFAULT TRUE | Account status |
| created_at | TIMESTAMP | NOT NULL | Record creation |
| updated_at | TIMESTAMP | NOT NULL | Last update |

### Relationships

- One User → One UserProfile
- One User → One Wallet
- One User → Many QuizAttempts
- One User → Many XPTransactions
- One User → Many WalletTransactions
- One User → Many UserBadges
- One User → Many UserAchievements
- One User → Many SavingsGoals

### Business Rules

- Email must be unique.
- Username must be unique.
- Password is never stored in plain text.
- Deleted accounts are soft deleted.

### Example Record

```json
{
  "id": "2f4d4f67...",
  "email": "alex@example.com",
  "username": "Alex23",
  "role": "student",
  "is_verified": true,
  "is_active": true
}
```

---

# 4.2 UserProfile

## Category

Core Entity

### Purpose

Stores personal information separate from authentication.

### Attributes

| Column | Type |
|--------|------|
| id | UUID |
| user_id | UUID |
| first_name | VARCHAR(100) |
| last_name | VARCHAR(100) |
| avatar_url | TEXT |
| country | VARCHAR(100) |
| language | VARCHAR(20) |
| grade | VARCHAR(20) |
| created_at | TIMESTAMP |
| updated_at | TIMESTAMP |

### Relationships

One UserProfile belongs to one User.

### Business Rules

Every user has exactly one profile.

---

# 4.3 Course

## Category

Core Entity

### Purpose

Represents a complete learning course.

### Attributes

| Column | Type |
|--------|------|
| id | UUID |
| title | VARCHAR(200) |
| description | TEXT |
| difficulty | VARCHAR(20) |
| estimated_minutes | INTEGER |
| is_published | BOOLEAN |
| created_at | TIMESTAMP |

### Relationships

One Course

↓

Many Modules

---

# 4.4 Module

## Category

Core Entity

Contains lessons within a course.

Relationships:

Course

↓

Module

↓

Lesson

---

# 4.5 Lesson

## Category

Core Entity

Stores educational lessons.

Relationships

Module

↓

Lesson

↓

Quiz

---

# 4.6 Quiz

## Category

Core Entity

Stores quizzes attached to lessons.

Relationships

Lesson

↓

Quiz

↓

Questions

---

# 4.7 Question

## Category

Core Entity

Stores quiz questions.

Relationships

Quiz

↓

Questions

↓

Answer Options

---

# 4.8 AnswerOption

Stores multiple-choice answers.

Correct answer identified using:

is_correct BOOLEAN

---

# 4.9 QuizAttempt

## Category

Transactional

Records every quiz attempt.

Characteristics

Immutable.

Never updated after completion.

---

# 4.10 QuizAnswer

Transactional.

Stores each answer submitted during an attempt.

---

# 4.11 Wallet

Core Entity.

Each user owns exactly one wallet.

Stores current virtual balance.

---

# 4.12 WalletTransaction

Transactional.

Stores deposits, rewards, spending, penalties.

Never edited.

---

# 4.13 XPTransaction

Transactional.

Stores every XP event.

Examples:

+50 XP

+10 XP

-20 XP

Used to calculate total XP.

---

# 4.14 Badge

Reference Entity.

Stores badge definitions.

Examples:

First Quiz

Budget Master

Investor

---

# 4.15 UserBadge

Junction Entity.

Connects:

User

↓

Badge

Stores:

earned_at

---

# 4.16 Achievement

Reference Entity.

Defines achievements.

---

# 4.17 UserAchievement

Junction Entity.

Connects:

User

↓

Achievement

---

# 4.18 Level

Reference Entity.

Defines XP thresholds.

Example:

Level 1

0 XP

Level 2

250 XP

Level 3

700 XP

etc.

---

# 4.19 Budget

Core Entity.

Represents a user's budget.

---

# 4.20 BudgetCategory

Reference Entity.

Examples:

Food

Transport

Entertainment

Education

Savings

---

# 4.21 SavingsGoal

Core Entity.

Represents a personal savings goal.

---

# 4.22 GoalContribution

Transactional.

Stores contributions toward savings goals.

---

# 4.23 Challenge

Reference Entity.

Defines challenges.

---

# 4.24 UserChallenge

Junction Entity.

Stores challenge participation and completion.

---

# 4.25 DailyStreak

Transactional.

Tracks consecutive learning days.

---

# 4.26 Notification

Transactional.

Stores in-app notifications.

---

# 4.27 RefreshToken

Transactional.

Stores refresh token metadata for secure authentication.

---

# 4.28 PasswordResetToken

Transactional.

Stores password reset requests.

---

# 4.29 UserPreference

Core Entity.

Stores configurable user preferences such as language, theme, notification settings, and learning preferences.

---

# 4.30 AIRecommendation

Transactional (Future).

Stores personalized recommendations generated by the AI engine.

---

# 4.31 LearningPath

Reference (Future).

Represents predefined or AI-generated learning paths.

---

# 4.32 Feedback

Transactional.

Stores user-submitted feedback.

---

# 4.33 AuditLog

Transactional.

Records important system actions for monitoring and security.

---

# 4.34 AppSetting

Reference Entity.

Stores configurable application-wide settings.

---

# 5. Summary

This document specifies every entity within the SmartCent database and defines its role within the system. Together with the Database Design document, it provides a complete logical data model that can be translated into PostgreSQL tables, SQLAlchemy models, FastAPI schemas, and the Entity Relationship Diagram (ERD).

The next step is to produce the **ENTITY_RELATIONSHIP_DIAGRAM.md**, which will visualize these entities and their relationships before physical database implementation.