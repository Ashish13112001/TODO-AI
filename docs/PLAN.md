# Todo List Application - Development Plan

## 1. Purpose

This document defines the development phases, project structure, and implementation order for the Todo List Application.

The project must be developed **incrementally, one phase at a time**.

### Important Rules

* Do NOT implement the entire application at once.
* Do NOT skip phases.
* Do NOT implement future-phase features unless explicitly requested.
* Complete and validate the current phase before moving to the next phase.
* If a requirement is unclear, ask for clarification before implementing it.
* Keep the implementation simple and consistent with the project architecture.
* Follow the defined folder structure.
* Do NOT create unnecessary files or folders.
* Do NOT move files between folders without a valid architectural reason.

---

# 2. Development Flow

```text
Phase 1
Project Setup
     ↓
Phase 2
Backend Setup
     ↓
Phase 3
Database Setup
     ↓
Phase 4
Todo API
     ↓
Phase 5
Frontend Setup
     ↓
Phase 6
Frontend UI
     ↓
Phase 7
API Integration
     ↓
Phase 8
Testing & Validation
     ↓
Phase 9
Final Cleanup
```

---

# 3. Project Structure

The application will use a separate frontend and backend structure.

```text
todo-app/
│
├── .cursor/
│   └── rules/
│       └── project-rules.mdc
│
├── docs/
│   ├── PLAN.md
│   ├── PROJECT_DOCUMENTATION.md
│   └── API.md
│
├── frontend/
│   ├── public/
│   │
│   └── src/
│       ├── assets/
│       ├── components/
│       ├── pages/
│       ├── services/
│       ├── hooks/
│       ├── types/
│       ├── utils/
│       ├── App.tsx
│       ├── main.tsx
│       └── index.css
│
├── backend/
│   ├── src/
│   │   ├── config/
│   │   ├── controllers/
│   │   ├── middleware/
│   │   ├── models/
│   │   ├── routes/
│   │   ├── services/
│   │   ├── types/
│   │   ├── utils/
│   │   ├── app.ts
│   │   └── server.ts
│   │
│   └── package.json
│
├── .env.example
├── .gitignore
├── README.md
└── package.json
```

---

## 3.1 Folder Responsibilities

### `.cursor/`

Contains Cursor-specific project rules.

```text
.cursor/
└── rules/
    └── project-rules.mdc
```

Cursor should read and follow these rules while working on the project.

---

### `docs/`

Contains project documentation.

```text
docs/
├── PLAN.md
├── PROJECT_DOCUMENTATION.md
└── API.md
```

* `PLAN.md` → Development phases and implementation order.
* `PROJECT_DOCUMENTATION.md` → Overall project requirements and technical documentation.
* `API.md` → API endpoint documentation.

Documentation should be committed to Git.

---

### `frontend/`

Contains the React application.

```text
frontend/
└── src/
    ├── assets/
    ├── components/
    ├── pages/
    ├── services/
    ├── hooks/
    ├── types/
    └── utils/
```

#### `components/`

Reusable UI components.

Example:

```text
components/
├── TodoForm/
├── TodoItem/
└── TodoList/
```

#### `pages/`

Application-level pages.

Example:

```text
pages/
└── TodoPage/
```

#### `services/`

API communication.

Example:

```text
services/
└── todoService.ts
```

#### `hooks/`

Custom React hooks.

Example:

```text
hooks/
└── useTodos.ts
```

#### `types/`

Frontend TypeScript types/interfaces.

Example:

```text
types/
└── todo.ts
```

#### `utils/`

Reusable utility functions.

---

### `backend/`

Contains the Node.js + Express backend.

```text
backend/
└── src/
    ├── config/
    ├── controllers/
    ├── middleware/
    ├── models/
    ├── routes/
    ├── services/
    ├── types/
    └── utils/
```

#### `config/`

Application and database configuration.

Example:

```text
config/
└── database.ts
```

#### `controllers/`

Handle HTTP requests and responses.

Example:

```text
controllers/
└── todoController.ts
```

#### `models/`

Database models/schemas.

Example:

```text
models/
└── todoModel.ts
```

#### `routes/`

API route definitions.

Example:

```text
routes/
└── todoRoutes.ts
```

#### `services/`

Business logic.

Example:

```text
services/
└── todoService.ts
```

#### `middleware/`

Express middleware.

Example:

```text
middleware/
├── errorMiddleware.ts
└── notFoundMiddleware.ts
```

#### `types/`

Backend TypeScript types/interfaces.

#### `utils/`

Reusable backend utility functions.

---

# 4. Folder Creation Rules

Folders should be created **only when they are required by the current phase**.

For example, during Phase 2:

```text
backend/
└── src/
    ├── config/
    ├── middleware/
    ├── routes/
    ├── app.ts
    └── server.ts
```

Do NOT create every possible file immediately.

For example, do NOT create:

```text
todoController.ts
todoService.ts
todoModel.ts
todoRoutes.ts
```

until the relevant phase requires them.

The folder structure defines the **architecture**, while each phase determines **when the files are created**.

---

# 5. Development Phases

## Phase 1 — Project Setup

### Goal

Create the basic project structure and configure the development environment.

### Tasks

* [ ] Create project root.
* [ ] Initialize Git repository.
* [ ] Create `.gitignore`.
* [ ] Create `README.md`.
* [ ] Create `docs/`.
* [ ] Create `.cursor/rules/`.
* [ ] Create `frontend/`.
* [ ] Create `backend/`.
* [ ] Initialize frontend project.
* [ ] Initialize backend project.
* [ ] Configure TypeScript.
* [ ] Create `.env.example`.

### Expected Structure

```text
todo-app/
├── .cursor/
├── docs/
├── frontend/
├── backend/
├── .env.example
├── .gitignore
└── README.md
```

### Do Not Implement

* Todo functionality
* Database models
* API endpoints
* Todo UI
* Authentication

---

## Phase 2 — Backend Setup

### Goal

Create and configure the Express backend.

### Tasks

* [ ] Configure Express.
* [ ] Create `server.ts`.
* [ ] Create `app.ts`.
* [ ] Configure environment variables.
* [ ] Create basic middleware.
* [ ] Create `config/`.
* [ ] Create `middleware/`.
* [ ] Create `routes/`.
* [ ] Configure basic error handling.
* [ ] Verify backend starts successfully.

### Expected Structure

```text
backend/
└── src/
    ├── config/
    ├── middleware/
    ├── routes/
    ├── app.ts
    └── server.ts
```

### Do Not Implement

* Todo CRUD
* Database integration
* Authentication
* Frontend integration

---

## Phase 3 — Database Setup

### Goal

Connect the backend to the database and create the Todo data model.

### Tasks

* [ ] Configure database connection.
* [ ] Add database configuration inside `config/`.
* [ ] Create `models/`.
* [ ] Create Todo model.
* [ ] Define Todo fields.
* [ ] Define validations.
* [ ] Test database connection.

### Expected Structure

```text
backend/
└── src/
    ├── config/
    │   └── database.ts
    ├── models/
    │   └── todoModel.ts
    ├── middleware/
    ├── routes/
    ├── app.ts
    └── server.ts
```

---

## Phase 4 — Todo API

### Goal

Create the REST API for Todo management.

### Tasks

* [ ] Create `todoController.ts`.
* [ ] Create `todoService.ts`.
* [ ] Create `todoRoutes.ts`.
* [ ] Implement `GET /todos`.
* [ ] Implement `GET /todos/:id`.
* [ ] Implement `POST /todos`.
* [ ] Implement `PATCH /todos/:id`.
* [ ] Implement `DELETE /todos/:id`.
* [ ] Add request validation.
* [ ] Add error handling.
* [ ] Test all Todo endpoints.

### Expected Structure

```text
backend/
└── src/
    ├── config/
    ├── controllers/
    │   └── todoController.ts
    ├── middleware/
    ├── models/
    │   └── todoModel.ts
    ├── routes/
    │   └── todoRoutes.ts
    ├── services/
    │   └── todoService.ts
    ├── types/
    ├── utils/
    ├── app.ts
    └── server.ts
```

---

## Phase 5 — Frontend Setup

### Goal

Create and configure the React frontend.

### Tasks

* [ ] Initialize React application.
* [ ] Configure TypeScript.
* [ ] Configure styling.
* [ ] Create `components/`.
* [ ] Create `pages/`.
* [ ] Create `services/`.
* [ ] Create `hooks/`.
* [ ] Create `types/`.
* [ ] Create `utils/`.
* [ ] Verify frontend runs successfully.

### Expected Structure

```text
frontend/
└── src/
    ├── assets/
    ├── components/
    ├── pages/
    ├── services/
    ├── hooks/
    ├── types/
    ├── utils/
    ├── App.tsx
    ├── main.tsx
    └── index.css
```

---

## Phase 6 — Frontend UI

### Goal

Build the Todo user interface.

### Tasks

* [ ] Create Todo page.
* [ ] Create Todo list.
* [ ] Create Todo item.
* [ ] Create Todo form.
* [ ] Add create Todo UI.
* [ ] Add edit Todo UI.
* [ ] Add delete Todo UI.
* [ ] Add complete/incomplete UI.
* [ ] Add loading state.
* [ ] Add empty state.
* [ ] Add error state.
* [ ] Make UI responsive.

### Expected Structure

```text
frontend/
└── src/
    ├── components/
    │   ├── TodoForm/
    │   ├── TodoItem/
    │   └── TodoList/
    ├── pages/
    │   └── TodoPage/
    ├── services/
    ├── hooks/
    ├── types/
    └── utils/
```

Use local/mock data during this phase.

Do NOT connect the frontend to the backend yet.

---

## Phase 7 — Frontend API Integration

### Goal

Connect the React frontend to the backend Todo API.

### Tasks

* [ ] Create `todoService.ts`.
* [ ] Create API client if required.
* [ ] Create `todo.ts` types.
* [ ] Connect GET API.
* [ ] Connect POST API.
* [ ] Connect PATCH API.
* [ ] Connect DELETE API.
* [ ] Handle loading states.
* [ ] Handle API errors.
* [ ] Verify end-to-end functionality.

### Expected Flow

```text
React Component
      ↓
Custom Hook
      ↓
Service/API Client
      ↓
Express API
      ↓
Controller
      ↓
Service
      ↓
Database
```

---

## Phase 8 — Testing & Validation

### Goal

Verify that the application works correctly.

### Tasks

* [ ] Test Todo creation.
* [ ] Test Todo retrieval.
* [ ] Test Todo update.
* [ ] Test Todo deletion.
* [ ] Test Todo completion.
* [ ] Test invalid requests.
* [ ] Test API errors.
* [ ] Test frontend errors.
* [ ] Test responsive UI.
* [ ] Fix discovered bugs.

---

## Phase 9 — Final Cleanup

### Goal

Prepare the project for GitHub and final delivery.

### Tasks

* [ ] Remove unused code.
* [ ] Remove unused dependencies.
* [ ] Review folder structure.
* [ ] Review environment configuration.
* [ ] Verify `.gitignore`.
* [ ] Update `README.md`.
* [ ] Update `docs/`.
* [ ] Add setup instructions.
* [ ] Add API documentation.
* [ ] Run final tests.
* [ ] Verify production build.
* [ ] Commit final changes.

---

# 6. Phase Execution Rule

Cursor must work on **one phase at a time**.

When the user says:

```text
Implement Phase 1
```

Cursor should:

```text
Read project-rules.mdc
        ↓
Read PLAN.md
        ↓
Identify Phase 1
        ↓
Implement ONLY Phase 1
        ↓
Validate Phase 1
        ↓
Report completion
        ↓
STOP
```

Cursor must NOT automatically continue to Phase 2.

The next phase can only be started when the user explicitly requests it.

---

# 7. Phase Completion Format

After completing a phase, Cursor should report:

```text
Phase: <phase name>

Completed:
- Task 1 ✓
- Task 2 ✓
- Task 3 ✓

Files Created/Modified:
- file/path
- file/path

Validation:
- Check 1 ✓
- Check 2 ✓

Status: COMPLETE

Next Phase:
<next phase>

Waiting for user instruction.
```
