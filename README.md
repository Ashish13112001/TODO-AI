# Todo List Application

A simple Todo List web application using the MERN stack with TypeScript.

This project is developed incrementally. See `docs/PLAN.md` for the phase order.

## Stack

- Frontend: React, Vite, TypeScript, Tailwind CSS
- Backend: Node.js, Express.js, TypeScript
- Database: MongoDB, Mongoose

## Current status

Phase 1 — Project Setup is complete. Frontend and backend packages are initialized with TypeScript. Application features are not implemented yet.

## Project structure

```text
todo-app/
├── .cursor/rules/
├── docs/
├── frontend/
├── backend/
├── .env.example
├── .gitignore
└── README.md
```

## Setup

1. Copy `.env.example` to `.env` and adjust values as needed.
2. Install frontend dependencies:

```bash
cd frontend
npm install
```

3. Install backend dependencies:

```bash
cd backend
npm install
```

## Scripts

Frontend (`frontend/`):

- `npm run dev` — start the Vite dev server
- `npm run build` — production build
- `npm run preview` — preview the production build

Backend (`backend/`):

- `npm run typecheck` — TypeScript check
- `npm run build` — compile TypeScript (no application source yet)

## Documentation

- `docs/PLAN.md` — development phases
- `docs/REQUIREMENTS.md` — product requirements
- `docs/IMPLEMENTATION.md` — implementation guide
