# SmartCent Database Design

**Document Version:** 1.0

**Project:** SmartCent

**Phase:** System Design

**Status:** Draft

---

# 1. Purpose

The Database Design document defines the logical structure of SmartCent's data layer. It identifies the major business entities, establishes relationships between them, specifies naming conventions, and outlines the principles that govern data storage throughout the application.

This document serves as the foundation for:

- Entity Relationship Diagram (ERD)
- PostgreSQL Schema
- Backend API Development
- Authentication
- Gamification
- Financial Simulation
- Analytics
- Future System Expansion

---

# 2. Objectives

The SmartCent database is designed to:

- Store data accurately and consistently.
- Minimize redundancy through normalization.
- Support high-performance querying.
- Maintain referential integrity.
- Scale as new features are introduced.
- Protect sensitive user information.
- Remain easy to understand and maintain.

---

# 3. Database Type

SmartCent uses a relational database management system (RDBMS).

Chosen Database:

**PostgreSQL**

Reasons:

- ACID compliant
- Excellent performance
- Mature ecosystem
- Strong indexing support
- JSON support where needed
- Robust security
- Excellent compatibility with FastAPI

---

# 4. Design Principles

The following principles guide every design decision.

## 4.1 Single Responsibility

Each table represents one business concept only.

Examples:

- User
- Lesson
- Wallet
- Badge

Never combine multiple concepts into one table.

---

## 4.2 Data Integrity

Relationships are enforced using foreign keys.

Duplicate information should be avoided.

Every record must have one authoritative source.

---

## 4.3 Scalability

The schema should support:

- thousands of users
- thousands of lessons
- millions of quiz attempts
- future learning content
- future AI features

without structural redesign.

---

## 4.4 Security

Sensitive information will never be stored in plain text.

Passwords:

Stored as secure password hashes.

Authentication:

JWT Access Tokens

Refresh Tokens

Secure password reset flow

---

## 4.5 Extensibility

The design should allow future additions such as:

- investment simulator
- classroom support
- teacher dashboards
- parent accounts
- leaderboards
- achievements
- multiplayer challenges
- AI tutoring

without breaking existing tables.

---

# 5. Database Domains

The SmartCent database is divided into independent business domains.

This improves maintainability and keeps related entities together.

## Authentication

Responsible for user identity and security.

Entities:

- User
- RefreshToken
- PasswordResetToken

---

## User Profile

Stores profile information and user preferences.

Entities:

- UserProfile
- UserPreference

---

## Learning

Contains educational content.

Entities:

- Course
- Module
- Lesson
- LessonContent

---

## Quiz Engine

Responsible for quizzes and assessments.

Entities:

- Quiz
- Question
- AnswerOption
- QuizAttempt
- QuizAnswer

---

## Gamification

Tracks user progress and motivation.

Entities:

- Level
- Badge
- UserBadge
- Achievement
- UserAchievement
- XPTransaction

---

## Wallet

Virtual money simulation.

Entities:

- Wallet
- WalletTransaction

---

## Budgeting

Budget management.

Entities:

- Budget
- BudgetCategory

---

## Savings

Savings goals and contributions.

Entities:

- SavingsGoal
- GoalContribution

---

## Challenges

Daily and weekly engagement.

Entities:

- Challenge
- UserChallenge
- DailyStreak

---

## Notifications

Stores notifications.

Entities:

- Notification

---

## AI

Future recommendation engine.

Entities:

- AIRecommendation
- LearningPath

---

## Administration

Administrative data.

Entities:

- Feedback
- AuditLog
- AppSetting

---

# 6. Entity Inventory

| Domain | Entity |
|---------|----------|
| Authentication | User |
| Authentication | RefreshToken |
| Authentication | PasswordResetToken |
| Profile | UserProfile |
| Profile | UserPreference |
| Learning | Course |
| Learning | Module |
| Learning | Lesson |
| Learning | LessonContent |
| Quiz | Quiz |
| Quiz | Question |
| Quiz | AnswerOption |
| Quiz | QuizAttempt |
| Quiz | QuizAnswer |
| Gamification | Level |
| Gamification | Badge |
| Gamification | UserBadge |
| Gamification | Achievement |
| Gamification | UserAchievement |
| Gamification | XPTransaction |
| Wallet | Wallet |
| Wallet | WalletTransaction |
| Budget | Budget |
| Budget | BudgetCategory |
| Savings | SavingsGoal |
| Savings | GoalContribution |
| Challenges | Challenge |
| Challenges | UserChallenge |
| Challenges | DailyStreak |
| Notifications | Notification |
| AI | AIRecommendation |
| AI | LearningPath |
| Administration | Feedback |
| Administration | AuditLog |
| Administration | AppSetting |

Total Planned Entities: **34**

---

# 7. Naming Conventions

## Tables

Singular.

Examples:

- user
- lesson
- badge
- wallet

---

## Primary Keys

Every table contains:

id

(UUID)

---

## Foreign Keys

Always use:

entity_name_id

Examples:

- user_id
- lesson_id
- wallet_id
- course_id

---

## Date Fields

Standard timestamps:

- created_at
- updated_at
- deleted_at
- completed_at
- expires_at

---

## Boolean Fields

Prefix with:

is_

Examples:

- is_active
- is_verified
- is_completed
- is_locked

---

## Monetary Values

All monetary values use:

NUMERIC(12,2)

Never FLOAT.

---

# 8. Common Columns

Most business tables contain:

| Column | Purpose |
|----------|------------|
| id | Primary key |
| created_at | Record creation |
| updated_at | Last modification |
| deleted_at | Soft delete |
| is_active | Active status |

Audit tables may contain additional metadata.

---

# 9. Relationship Strategy

Relationships use foreign keys.

Relationship types include:

### One-to-One

Example:

User → UserProfile

---

### One-to-Many

Example:

Course → Modules

Module → Lessons

Lesson → Quizzes

Wallet → Transactions

---

### Many-to-Many

Resolved using junction tables.

Examples:

User ↔ Badge

User ↔ Achievement

User ↔ Challenge

---

# 10. Normalization

The database targets Third Normal Form (3NF).

This ensures:

- no duplicated data
- no repeating groups
- reduced update anomalies
- easier maintenance

Denormalization will only be introduced if justified by performance requirements.

---

# 11. Indexing Strategy

Indexes improve query performance.

Primary indexes:

- Primary Keys
- Foreign Keys

Additional indexes:

- email
- username
- created_at
- lesson_id
- user_id

Composite indexes may be added after performance testing.

---

# 12. Security Considerations

Passwords are hashed using a strong password hashing algorithm.

Access Tokens are short-lived JWTs.

Refresh Tokens are stored securely and can be revoked.

Sensitive data is minimized.

No payment information is stored in the MVP.

The wallet represents virtual educational currency only.

---

# 13. Future Expansion

The database has been designed to support future modules including:

- Friends
- Messaging
- Investment Simulator
- Teacher Portal
- Parent Portal
- Classroom Management
- Financial Challenges
- Marketplace
- AI Tutor
- Offline Synchronization
- Multi-language Content

without major structural changes.

---

# 14. Summary

This document defines the logical database architecture for SmartCent.

It establishes:

- database philosophy
- design principles
- domains
- entity inventory
- naming conventions
- relationship strategy
- normalization rules
- indexing strategy
- security considerations

The next document, **ENTITY_SPECIFICATIONS.md**, will define every entity in detail, including columns, data types, constraints, and business rules. Once complete, these specifications will be used to produce the Entity Relationship Diagram (ERD) and the physical PostgreSQL schema.