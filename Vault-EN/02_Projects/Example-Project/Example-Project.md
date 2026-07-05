---
created: 2026-01-01
modified: 2026-07-02
type: project
status: 🟡 In Progress
deadline: 2026-03-01
tags:
  - project
related_knowledge:
  - "[[03_Knowledge/Example-Topic/Example-Topic]]"
related_snippets:
  - "[[04_Snippets/Hello-World-FastAPI]]"
repo: https://github.com/yourusername/example-project
---

# Example-Project

> [!abstract] Project Summary
> Building a minimal REST API with FastAPI to demonstrate how projects are tracked in this vault.

---

## Goals

- [x] #task Set up project structure  [due:: 2026-01-05]  [completion:: 2026-07-02]
- [ ] #task Create first endpoint  [due:: 2026-01-10]
- [x] #task Write tests  [due:: 2026-01-20]  [completion:: 2026-07-02]
- [ ] #task Deploy to production  [due:: 2026-03-01]
- [x] #bug 
- [ ] 
- [ ] #

---

## Milestones

| Date       | Target              | Status |
|------------|---------------------|--------|
| 2026-01-10 | Core API working    | 🟢     |
| 2026-02-01 | Tests passing       | 🔴     |
| 2026-03-01 | Production deploy   | 🔴     |

---

## Technical Decisions
_Why FastAPI instead of Flask? FastAPI offers async support natively and auto-generates OpenAPI docs._

- Chose Pydantic v2 for validation — stricter types, better performance
- SQLite for dev, PostgreSQL for prod

---

## Open Questions

- Should we add authentication in v1 or v2?
- Which deployment platform: Railway, Fly.io, or VPS?

---

## Links

- Related Theory: [[03_Knowledge/Example-Topic/Example-Topic]]
- Related Snippet: [[04_Snippets/Hello-World-FastAPI]]
- Repo / Link: https://github.com/yourusername/example-project

---

## Progress Log

### 2026-01-10
_Built the core API structure. GET /items endpoint working. Need to add POST next._

- Completed: project scaffold, main.py, router structure
- Blocked on: database schema decisions

### 2026-01-01
_Project kick-off. Decided on FastAPI + SQLite stack._

-
