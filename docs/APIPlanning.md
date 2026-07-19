# Software Architecture

# PLANWISE
AI-Powered Study Planner

Version: 1.0

---

# 1. Overview

PLANWISE follows a three-tier architecture consisting of:

- Frontend (Presentation Layer)
- Backend (Business Logic Layer)
- Database (Data Layer)

Artificial Intelligence services are integrated through external APIs.

---

# 2. Architecture Layers

## Presentation Layer (Frontend)

Technology:
- React.js
- HTML5
- CSS3
- JavaScript

Responsibilities:
- User Interface
- Forms
- Dashboard
- Calendar
- Analytics
- Communicate with Backend APIs

---

## Business Logic Layer (Backend)

Technology:
- Java
- Spring Boot

Responsibilities:

- Authentication
- Authorization
- AI Integration
- Timetable Generation
- Progress Calculation
- API Development
- Business Rules

---

## Data Layer

Technology:
- MySQL

Responsibilities:

- Store Users
- Store Subjects
- Store Exams
- Store Study Plans
- Store Progress
- Store AI Recommendations

---

# 3. External Services

## OpenAI API

Purpose:

- Generate study plans
- Study suggestions
- Motivation
- Revision schedules

---

# 4. Authentication

Authentication Method:

- JWT (JSON Web Token)

Security Features:

- Password Encryption
- Secure Login
- Token Validation
- Protected APIs

---

# 5. API Communication

Frontend

↓

REST API

↓

Spring Boot Backend

↓

MySQL Database

↓

Response returned to Frontend

---

# 6. Folder Structure

PLANWISE

frontend/

backend/

database/

docs/

assets/

---

# 7. High-Level Workflow

1. User logs in.

2. Authentication is verified.

3. User accesses dashboard.

4. User adds subjects and exams.

5. Backend stores information.

6. User requests AI study plan.

7. Backend sends request to AI.

8. AI generates study plan.

9. Backend saves study plan.

10. Frontend displays timetable.

11. User marks tasks completed.

12. Progress analytics update automatically.

---

# 8. Scalability

Future improvements include:

- Mobile App

- Notification Service

- AI Chatbot

- Cloud Deployment

- Real-Time Sync

- Collaborative Study Groups

---

# 9. Security

The system will provide:

- JWT Authentication

- Password Hashing

- Input Validation

- SQL Injection Protection

- Cross-Site Request Forgery Protection

- HTTPS Communication

---

# 10. Conclusion

The architecture of PLANWISE follows modern full-stack development principles, ensuring modularity, scalability, maintainability, and security.

The layered architecture allows independent development of the frontend, backend, and database while supporting future feature expansion.
