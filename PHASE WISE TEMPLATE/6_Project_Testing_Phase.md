# Phase 6: Project Testing Phase

## 1. Unit & Integration Testing
* Tested `/api/faq/ask` with simple and complex prompt structures.
* Verified token extraction and validation on protected routes (`/api/faq/all`).

## 2. API Endpoint Testing Matrix
| Endpoint | Method | Auth Required | Test Payload | Expected Status |
| :--- | :--- | :--- | :--- | :--- |
| `/api/auth/login` | POST | No | `{ "username": "admin", ... }` | 200 OK |
| `/api/faq/ask` | POST | No | `{ "question": "What is AI?" }` | 200 OK |
| `/api/faq/all` | GET | Yes | Header: `Bearer <token>` | 200 OK |
| `/api/faq/all` | GET | No | None | 401 Unauthorized |