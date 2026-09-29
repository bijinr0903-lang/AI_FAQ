# Phase 3: Project Design Phase

## 1. System Architecture
```
[ Client / Web App ]
       │
       ▼
[ Express Router ]
       │
   ┌───┴────────────────────────┐
   ▼                            ▼
[ Public Routes ]      [ Auth Middleware ]
   │                            │
   ▼                            ▼
[ FAQ Controller ]     [ Protected Routes ]
   │
   ▼
[ Gemini AI Service ]
```

## 2. API Endpoint Schema
* `POST /api/auth/login` - Admin login generating JWT bearer token.
* `POST /api/faq/ask` - Submit question and retrieve Gemini AI output.
* `GET /api/faq/all` - Fetch saved/cached FAQ records (Requires JWT).