---
created: 2026-01-01
modified: 2026-07-02
type: knowledge
status: 🟡 Learning
tags:
  - backend/fastapi/routing
parent: "[[Backend]]"
children:
  - "[[Dependency Injection]]"
  - "[[FastAPI Middleware]]"
related_theory:
  - "[[Pydantic Models]]"
related_snippets:
  - "[[04_Snippets/Hello-World-FastAPI]]"
related_projects:
  - "[[02_Projects/Example-Project/Example-Project]]"
source: https://fastapi.tiangolo.com/tutorial/
---

# Example-Topic

> [!abstract] One Sentence
> FastAPI routing defines URL endpoints using Python decorators, supporting path parameters, query strings, and automatic OpenAPI generation.

---

## Theory

### What?
FastAPI routing maps HTTP methods and URL paths to Python functions called "path operations".

### Why?
Decouples request handling from business logic. Each route is a clean, typed function.

### How does it work?
1. Define a FastAPI app instance
2. Use decorators (`@app.get`, `@app.post`, etc.) on functions
3. FastAPI generates OpenAPI docs automatically
4. Pydantic models validate request/response bodies

### When to use?
Whenever you need to expose an HTTP API. Prefer FastAPI over Flask when you need async support or automatic validation.

---

## Key Points

- Path parameters: `@app.get("/items/{item_id}")`
- Query parameters: defined as function arguments with defaults
- Response models: use `response_model=` for automatic serialization
- Routers: use `APIRouter` to split large APIs into modules

---

## Parameters / Configuration

| Parameter      | Description                    | Default | Notes               |
|----------------|--------------------------------|---------|---------------------|
| `prefix`       | URL prefix for a router        | ""      | e.g. `/api/v1`      |
| `tags`         | OpenAPI grouping               | []      | Shown in /docs      |
| `dependencies` | Shared dependency injection    | []      | Auth, DB session    |

---

## Minimal Example

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/items/{item_id}")
def read_item(item_id: int, q: str = None):
    return {"item_id": item_id, "q": q}
```

> [!note] Takeaway
> FastAPI infers types from function signatures. No separate schema definition needed.

---

## Connections

**Theory tree:**
- Parent topic → [[Backend]]
- Child topics → [[Dependency Injection]], [[FastAPI Middleware]]
- Compare with → [[Flask Routing]]

**Practical:**
- Snippet → [[04_Snippets/Hello-World-FastAPI]]
- Project → [[02_Projects/Example-Project/Example-Project]]

---

## Tasks

- [x] #task Apply the concept with an example [due:: 2026-01-05]
- [ ] #task Write a middleware snippet [due:: 2026-01-15]
- [ ] #task Fill in the `children` field [due:: 2026-01-10]
- [ ] #task Update status when done

---

## Raw Notes

_Unresolved questions and rough thoughts._

- ? How does FastAPI handle versioning cleanly?
- ? Best pattern for shared database sessions?
