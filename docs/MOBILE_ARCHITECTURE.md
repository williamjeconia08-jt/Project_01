# SmartCent Mobile Architecture

**Document Version:** 1.0

**Project:** SmartCent

**Phase:** System Design

**Status:** Draft

---

# 1. Purpose

This document defines the architecture of the SmartCent Flutter application.

It specifies:

- Project structure
- State management
- Navigation
- Feature modules
- API communication
- Offline strategy
- Dependency management
- Error handling
- Security
- Future scalability

The goal is to build a maintainable, scalable and testable mobile application.

---

# 2. Technology Stack

| Component | Technology |
|------------|------------|
| Framework | Flutter |
| Language | Dart |
| State Management | Riverpod |
| Navigation | GoRouter |
| HTTP Client | Dio |
| Local Storage | Hive |
| Secure Storage | flutter_secure_storage |
| JSON Serialization | json_serializable |
| Dependency Injection | Riverpod Providers |
| Testing | flutter_test |

---

# 3. Architectural Style

SmartCent follows a

Feature-First Clean Architecture

Each feature contains its own:

- UI
- Business Logic
- Models
- Services
- Providers

Shared functionality lives in a common module.

---

# 4. Application Layers

Presentation

↓

Application

↓

Data

↓

API

↓

FastAPI Backend

---

## Presentation Layer

Contains:

- Screens
- Widgets
- Themes
- Navigation

---

## Application Layer

Contains:

- Providers
- Controllers
- Business Logic

---

## Data Layer

Contains:

- API Services
- Local Storage
- Models
- DTOs

---

# 5. Folder Structure

lib/

main.dart

app/

shared/

features/

core/

---

Detailed structure

lib/

├── main.dart

├── app/

│   ├── router.dart

│   ├── theme.dart

│   └── app.dart

│

├── core/

│   ├── constants/

│   ├── exceptions/

│   ├── network/

│   ├── storage/

│   ├── utils/

│   └── widgets/

│

├── shared/

│   ├── models/

│   ├── providers/

│   ├── services/

│   └── components/

│

├── features/

│   ├── authentication/

│   ├── onboarding/

│   ├── dashboard/

│   ├── learning/

│   ├── quizzes/

│   ├── wallet/

│   ├── budgeting/

│   ├── savings/

│   ├── gamification/

│   ├── challenges/

│   ├── notifications/

│   ├── profile/

│   └── settings/

```

Each feature has the same structure.

```
learning/

├── models/

├── providers/

├── repository/

├── services/

├── screens/

├── widgets/

└── controllers/

```

---

# 6. State Management

Riverpod manages application state.

Types of state:

- Authentication
- User
- Learning Progress
- Quiz State
- Wallet Balance
- Notifications
- Theme
- Network

State should never be stored directly inside UI widgets.

---

# 7. Navigation

Navigation uses GoRouter.

Example routes

/

↓

Onboarding

↓

Login

↓

Dashboard

↓

Learning

↓

Lesson

↓

Quiz

↓

Results

---

Protected routes require authentication.

---

# 8. API Communication

The application communicates only through the REST API.

Flutter

↓

Dio

↓

FastAPI

↓

PostgreSQL

The mobile application never accesses the database directly.

---

# 9. Local Storage

Hive stores:

- cached lessons
- user preferences
- app settings
- recently viewed lessons

Secure Storage stores:

- JWT
- Refresh Token

---

# 10. Authentication Flow

App Starts

↓

Check Secure Storage

↓

Token Exists?

↓

Yes

↓

Validate Token

↓

Dashboard

↓

No

↓

Login Screen

---

# 11. Error Handling

Errors are grouped into:

- Network Errors
- Validation Errors
- Authentication Errors
- Server Errors
- Unknown Errors

Every error displays a user-friendly message.

---

# 12. Theme Management

Support:

- Light Theme
- Dark Theme

Future:

- Dynamic Theme

---

# 13. Offline Support

The first release supports limited offline functionality.

Available offline:

- Cached lessons
- Cached profile
- Settings

Requires internet:

- Quizzes
- Wallet
- XP synchronization

Future versions may support full synchronization.

---

# 14. Performance

Strategies:

- Lazy loading
- Pagination
- Image caching
- Widget optimization
- Efficient state updates

---

# 15. Security

Sensitive data stored only in Secure Storage.

HTTPS only.

No secrets embedded inside the application.

Input validation occurs on both client and server.

---

# 16. Testing

Testing includes:

- Widget Tests
- Unit Tests
- Integration Tests

Critical features receive the highest coverage.

---

# 17. Scalability

The architecture supports:

- New learning modules
- AI tutoring
- Classroom features
- Parent portal
- Teacher dashboard
- Additional languages

No major restructuring should be necessary.

---

# 18. Summary

The SmartCent mobile application follows a feature-first architecture using Flutter, Riverpod, and GoRouter.

This modular design mirrors the backend architecture, ensuring consistency, maintainability, and scalability as the application grows.