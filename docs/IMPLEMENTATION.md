
---

# 3. `IMPLEMENTATION.md`

This file answers:

> **How should we implement the project?**

This is where we define architecture, coding conventions, folder structure, API conventions, etc.

```markdown
# Todo List Application - Implementation Guide

## 1. Purpose

This document defines how the Todo List application should be implemented.

It contains:

- Architecture
- Folder structure
- Coding conventions
- Backend structure
- Frontend structure
- API conventions
- Database conventions
- Environment configuration
- Error handling guidelines

This document should be followed by developers and AI coding assistants.

---

# 2. Architecture

The application follows a simple client-server architecture.

```text
                    ┌─────────────────────┐
                    │       Browser       │
                    │                     │
                    │ React + TypeScript  │
                    │ Tailwind CSS        │
                    └──────────┬──────────┘
                               │
                               │ HTTP / REST
                               ▼
                    ┌─────────────────────┐
                    │      Express        │
                    │      Backend        │
                    │                     │
                    │ Node.js + TypeScript│
                    └──────────┬──────────┘
                               │
                               │ Mongoose
                               ▼
                    ┌─────────────────────┐
                    │      MongoDB        │
                    │                     │
                    │      Todos          │
                    └─────────────────────┘