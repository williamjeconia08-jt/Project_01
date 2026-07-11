# SmartCent API Design

**Document Version:** 1.0

**Project:** SmartCent

**Phase:** System Design

**Status:** Draft

---

# 1. Purpose

This document defines the REST API architecture for SmartCent.

The API serves as the communication layer between the Flutter mobile application and the FastAPI backend.

It specifies:

- API architecture
- Versioning strategy
- Authentication
- Resource organization
- Endpoint conventions
- Request/Response formats
- Error handling
- Security standards

This document serves as the blueprint for backend implementation.

---

# 2. API Overview

Architecture Style:

REST API

Backend Framework:

FastAPI

Response Format:

JSON

Authentication:

JWT Authentication

Transport Protocol:

HTTPS

---

# 3. API Principles

The SmartCent API follows these principles.

## Stateless

Each request contains everything needed to process it.

The server does not store session state.

---

## Resource-Oriented

Resources are represented by nouns.

Good

GET /courses

Bad

GET /getCourses

---

## Predictable

Endpoints follow consistent naming and behavior.

---

## Secure

All authenticated endpoints require a valid JWT access token.

---

## Versioned

Every endpoint belongs to an API version.

Example:

/api/v1/

Future:

/api/v2/

---

# 4. Base URL

Development

http://localhost:8000/api/v1

Production

https://api.smartcent.app/api/v1

---

# 5. Authentication

Authentication uses JWT.

Flow:

Register

↓

Login

↓

Receive Access Token

↓

Receive Refresh Token

↓

Authenticated Requests

↓

Refresh Access Token

---

# 6. API Modules

The API is organized into feature modules rather than database entities.

Modules:

- Authentication
- User
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

Each module is independent and owns its endpoints.

---

# 7. Authentication API

Base Route

/api/v1/auth

Endpoints

POST /register

POST /login

POST /refresh

POST /logout

POST /forgot-password

POST /reset-password

GET /me

---

# 8. User API

Base Route

/api/v1/users

Endpoints

GET /profile

PUT /profile

PATCH /preferences

DELETE /account

---

# 9. Learning API

Base Route

/api/v1/learning

Endpoints

GET /courses

GET /courses/{id}

GET /modules/{id}

GET /lessons/{id}

GET /progress

POST /progress

---

# 10. Quiz API

Base Route

/api/v1/quizzes

Endpoints

GET /{quiz_id}

POST /start

POST /submit

GET /results/{attempt_id}

GET /history

---

# 11. Wallet API

Base Route

/api/v1/wallet

Endpoints

GET /balance

GET /transactions

POST /reward

POST /spend

---

# 12. Budget API

Base Route

/api/v1/budgets

Endpoints

GET /

POST /

PUT /{id}

DELETE /{id}

---

# 13. Savings API

Base Route

/api/v1/savings

Endpoints

GET /

POST /

GET /{id}

PUT /{id}

DELETE /{id}

POST /contribute

---

# 14. Gamification API

Base Route

/api/v1/gamification

Endpoints

GET /xp

GET /level

GET /badges

GET /achievements

GET /leaderboard

---

# 15. Challenge API

Base Route

/api/v1/challenges

Endpoints

GET /

POST /join

POST /complete

GET /daily

GET /weekly

---

# 16. Notification API

Base Route

/api/v1/notifications

Endpoints

GET /

PATCH /read

DELETE /{id}

---

# 17. AI API (Future)

Base Route

/api/v1/ai

Endpoints

GET /recommendations

GET /learning-path

POST /generate-plan

---

# 18. Administration API

Restricted to administrators.

Base Route

/api/v1/admin

Endpoints

GET /users

GET /analytics

GET /feedback

PATCH /settings

---

# 19. Standard HTTP Status Codes

| Code | Meaning |
|------|---------|
| 200 | Success |
| 201 | Resource Created |
| 204 | No Content |
| 400 | Bad Request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 409 | Conflict |
| 422 | Validation Error |
| 500 | Internal Server Error |

---

# 20. Standard Response Format

Successful responses follow a consistent structure.

Example

{
  "success": true,
  "message": "Course retrieved successfully.",
  "data": { }
}

Errors

{
  "success": false,
  "message": "Invalid credentials.",
  "errors": []
}

---

# 21. Pagination

Large collections support pagination.

Parameters

?page=1

&page_size=20

Response includes

- total_items
- total_pages
- current_page

---

# 22. Filtering

Example

GET /courses?difficulty=beginner

GET /transactions?type=reward

GET /lessons?module=3

---

# 23. Sorting

Example

?sort=name

?sort=-created_at

---

# 24. Security

HTTPS only

JWT Authentication

Password Hashing

Role-based authorization

Input validation

Rate limiting (future)

---

# 25. API Documentation

The API will automatically generate documentation using FastAPI.

Swagger UI

/docs

ReDoc

/redoc

---

# 26. Versioning Strategy

Current

/api/v1/

Future

/api/v2/

Breaking changes require a new API version.

---

# 27. Summary

The SmartCent REST API is organized around business features rather than database tables.

This modular approach keeps the backend scalable, maintainable, and aligned with the application's architecture.

The next document, BACKEND_ARCHITECTURE.md, will describe how these API modules are implemented within the FastAPI application, including project structure, service layers, dependency injection, and interaction with the PostgreSQL database.