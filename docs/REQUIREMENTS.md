# Todo List Application - Requirements

## 1. Project Overview

We are building a simple Todo List web application using the MERN stack with TypeScript.

The purpose of this project is to build a small full-stack application from scratch while following a structured, incremental development approach.

The application should allow users to create, view, update, delete, complete, and filter todos.

There is no authentication in the initial version.

---

## 2. Technology Stack

### Frontend

- React
- Vite
- TypeScript
- Tailwind CSS

### Backend

- Node.js
- Express.js
- TypeScript

### Database

- MongoDB
- Mongoose

### Development

- Git
- GitHub
- Cursor AI

---

## 3. Authentication

Authentication is NOT required in the initial version.

There will be:

- No registration
- No login
- No logout
- No JWT
- No sessions
- No user-specific todos

All todos belong to the single application.

Authentication may be added in a future version.

---

## 4. Todo Entity

Each todo should contain at least:

- `_id`
- `title`
- `description`
- `completed`
- `createdAt`
- `updatedAt`

### Todo fields

| Field | Type | Required | Description |
|---|---|---|---|
| `_id` | ObjectId | Yes | Unique todo identifier |
| `title` | String | Yes | Todo title |
| `description` | String | No | Additional information |
| `completed` | Boolean | Yes | Completion status |
| `createdAt` | Date | Yes | Creation timestamp |
| `updatedAt` | Date | Yes | Last update timestamp |

---

## 5. Core Features

### 5.1 Create Todo

The user should be able to create a new todo.

Required:

- Title

Optional:

- Description

A newly created todo should have:

```text
completed = false