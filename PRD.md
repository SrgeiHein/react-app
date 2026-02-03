# Product Requirements Document (PRD)

## Project: Simple Auth Flow

A minimal React application implementing forgot password and reset password functionality.

---

## Overview

This project demonstrates a simple authentication flow focused on password recovery:
1. User requests password reset via email
2. User receives reset link/code
3. User sets new password

---

## Features

### 1. Forgot Password Page
- Email input field
- Submit button
- Success message after submission
- Link back to login

### 2. Reset Password Page
- New password input
- Confirm password input
- Password strength indicator (optional)
- Submit button
- Success message with redirect to login

---

## Tech Stack

- **Frontend:** React + TypeScript + Vite
- **Styling:** CSS (or Tailwind if preferred)
- **Routing:** React Router
- **State:** React useState/useContext
- **API:** Mock API or simple fetch calls

---

## Pages

| Page | Route | Description |
|------|-------|-------------|
| Forgot Password | `/forgot-password` | Enter email to request reset |
| Reset Password | `/reset-password` | Enter new password |
| Success | `/success` | Confirmation page |

---

## Tasks

### Phase 1: Setup
- [ ] Install dependencies (react-router-dom)
- [ ] Setup routing structure
- [ ] Create basic page components

### Phase 2: Forgot Password
- [ ] Create ForgotPassword component
- [ ] Add email input with validation
- [ ] Add submit handler (mock API call)
- [ ] Show success/error states
- [ ] Style the page

### Phase 3: Reset Password
- [ ] Create ResetPassword component
- [ ] Add password + confirm password inputs
- [ ] Add password validation (min length, match)
- [ ] Add submit handler (mock API call)
- [ ] Show success/error states
- [ ] Style the page

### Phase 4: Polish
- [ ] Add loading states
- [ ] Add error handling
- [ ] Responsive design
- [ ] Test full flow

---

## UI Mockup (Text)

```
┌─────────────────────────────────────┐
│         Forgot Password             │
│                                     │
│  Enter your email to reset password │
│                                     │
│  ┌─────────────────────────────┐   │
│  │ email@example.com           │   │
│  └─────────────────────────────┘   │
│                                     │
│  ┌─────────────────────────────┐   │
│  │      Send Reset Link        │   │
│  └─────────────────────────────┘   │
│                                     │
│  ← Back to Login                    │
└─────────────────────────────────────┘
```

```
┌─────────────────────────────────────┐
│         Reset Password              │
│                                     │
│  Enter your new password            │
│                                     │
│  ┌─────────────────────────────┐   │
│  │ New Password                │   │
│  └─────────────────────────────┘   │
│                                     │
│  ┌─────────────────────────────┐   │
│  │ Confirm Password            │   │
│  └─────────────────────────────┘   │
│                                     │
│  ┌─────────────────────────────┐   │
│  │      Reset Password         │   │
│  └─────────────────────────────┘   │
└─────────────────────────────────────┘
```

---

## API Endpoints (Mock)

### POST /api/forgot-password
```json
Request:  { "email": "user@example.com" }
Response: { "success": true, "message": "Reset link sent" }
```

### POST /api/reset-password
```json
Request:  { "token": "abc123", "password": "newpass123" }
Response: { "success": true, "message": "Password updated" }
```

---

## Success Criteria

- [ ] User can submit email on forgot password page
- [ ] User sees confirmation after submitting email
- [ ] User can set new password on reset page
- [ ] Password validation works (min 8 chars, must match)
- [ ] User sees success message after reset
- [ ] Clean, simple UI
