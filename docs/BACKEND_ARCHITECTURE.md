# SmartCent Backend Architecture

**Document Version:** 1.0

**Project:** SmartCent

**Phase:** System Design

**Status:** Draft

---

# 1. Purpose

This document defines the internal architecture of the SmartCent backend.

It describes:

- Overall architecture
- Project structure
- Module organization
- Request lifecycle
- Layer responsibilities
- Dependency injection
- Database interaction
- Security architecture
- Error handling
- Logging
- Future scalability

---

# 2. Technology Stack

| Component | Technology |
|------------|------------|
| Language | Python 3.12+ |
| Framework | FastAPI |
| ORM | SQLAlchemy 2.x |
| Database | PostgreSQL |
| Validation | Pydantic |
| Authentication | JWT |
| Password Hashing | bcrypt |
| Database Migration | Alembic |
| Testing | Pytest |

---

# 3. Architectural Style

SmartCent uses a **Layered Modular Architecture**.

Each feature is divided into independent modules while sharing common infrastructure.

Benefits:

- Clear separation of concerns
- Easy testing
- Easier maintenance
- Independent feature development
- High scalability

---

# 4. High-Level Architecture

```

Flutter Mobile App

↓

REST API

↓

FastAPI Routers

↓

Service Layer

↓

Repository Layer

↓

SQLAlchemy ORM

↓

PostgreSQL Database

```

Each layer has a single responsibility.

---

# 5. Layer Responsibilities

## Presentation Layer

Handles HTTP communication.

Responsibilities:

- Receive requests
- Validate input
- Return responses
- Authenticate requests

Contains:

- API Routers

---

## Service Layer

Contains business logic.

Examples:

- XP calculations
- Quiz scoring
- Wallet rewards
- Budget validation
- Savings calculations

The Service Layer should not contain SQL queries.

---

## Repository Layer

Responsible for data access.

Responsibilities:

- Read data
- Write data
- Execute queries
- Hide database implementation details

Repositories should not contain business logic.

---

## Data Layer

Responsible for persistent storage.

Contains:

- SQLAlchemy Models
- PostgreSQL
- Alembic Migrations

---

# 6. Feature Modules

The backend is organized by business features.

Modules:

- Authentication
- Users
- Learning
- Quiz
- Wallet
- Budget
- Savings
- Gamification
- Challenges
- Notifications
- AI
- Administration

Each module contains its own routers, services, repositories, models, and schemas.

---

# 7. Proposed Project Structure

```

backend/

│

├── app/

│

├── api/

│   ├── auth.py
│   ├── users.py
│   ├── learning.py
│   ├── quizzes.py
│   ├── wallet.py
│   ├── budgets.py
│   ├── savings.py
│   ├── gamification.py
│   ├── challenges.py
│   ├── notifications.py
│   └── admin.py

│

├── services/

├── repositories/

├── models/

├── schemas/

├── core/

├── database/

├── middleware/

├── utils/

├── tests/

└── main.py

```

---

# 8. Module Structure

Every feature follows the same internal structure.

Example:

```

wallet/

├── router.py
├── service.py
├── repository.py
├── model.py
├── schema.py
└── exceptions.py

```

Benefits:

- Predictable
- Easy navigation
- Consistent development

---

# 9. Request Lifecycle

Example:

User taps:

"Complete Quiz"

↓

Flutter

↓

POST /quizzes/submit

↓

Quiz Router

↓

Quiz Service

↓

Quiz Repository

↓

Database

↓

Repository

↓

Service

↓

Router

↓

Flutter

---

# 10. Dependency Injection

FastAPI dependency injection is used for:

- Database sessions
- Authentication
- Current user
- Configuration
- Services

This reduces coupling between components.

---

# 11. Authentication Flow

1. User logs in.
2. Credentials are verified.
3. Password hash is checked.
4. JWT Access Token is created.
5. Refresh Token is generated.
6. Tokens are returned.
7. Protected endpoints validate JWT before processing.

---

# 12. Validation

Validation occurs using Pydantic models.

Responsibilities:

- Required fields
- Data types
- Email validation
- Length validation
- Business constraints

Invalid data never reaches the service layer.

---

# 13. Error Handling

Errors are standardized.

Example:

```

{
  "success": false,
  "message": "Quiz not found.",
  "errors": []
}

```

Common exceptions:

- ValidationError
- AuthenticationError
- AuthorizationError
- ResourceNotFoundError
- ConflictError

---

# 14. Logging

The backend logs:

- Login attempts
- Errors
- API requests
- Warnings
- System events

Sensitive information is never logged.

---

# 15. Security

Security measures include:

- HTTPS
- JWT Authentication
- Password hashing
- Input validation
- SQL injection prevention (ORM)
- CORS configuration
- Environment variables for secrets

Future enhancements:

- Rate limiting
- Two-factor authentication
- Email verification

---

# 16. Database Access

Only repositories interact directly with SQLAlchemy.

Services must never execute SQL.

This keeps business logic independent of database implementation.

---

# 17. Testing Strategy

Testing levels:

- Unit Tests
- Integration Tests
- API Tests

Each module should include tests for:

- Routers
- Services
- Repositories

---

# 18. Scalability

The architecture supports:

- Additional API versions
- Background workers
- WebSockets
- AI services
- Cloud deployment
- Microservice extraction (future)

No major restructuring should be required.

---

# 19. Design Principles

The backend follows these principles:

- Single Responsibility Principle (SRP)
- Separation of Concerns
- Dependency Inversion
- DRY (Don't Repeat Yourself)
- KISS (Keep It Simple)
- Explicit over implicit

---

# 20. Summary

The SmartCent backend uses a layered, modular architecture that separates HTTP handling, business logic, data access, and persistence into distinct responsibilities.

This design improves maintainability, testing, and scalability while providing a clear structure for future development.

The next document, MOBILE_ARCHITECTURE.md, will define how the Flutter application is organized, including folder structure, state management, navigation, feature modules, and communication with the backend API.