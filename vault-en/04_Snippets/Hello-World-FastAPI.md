---
created: 2026-01-01
modified: 2026-07-02
type: snippet
status: 🟢 Done
language: Python
domain: backend
dependencies:
  - fastapi
  - uvicorn
related_theory:
  - "[[03_Knowledge/Example-Topic/Example-Topic]]"
related_snippets: []
used_in_projects:
  - "[[02_Projects/Example-Project/Example-Project]]"
---

# Hello-World-FastAPI

> [!summary] What does it do?
> Minimal FastAPI app with one GET endpoint. The smallest working API you can run.

**Related Theory:** [[03_Knowledge/Example-Topic/Example-Topic]]
**Used In:** [[02_Projects/Example-Project/Example-Project]]

---

## Code

```python
# ==================================================
# SNIPPET: Hello World FastAPI
# Domain  : backend
# Language: Python
# Depends : fastapi, uvicorn
# ==================================================

from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def root():
    return {"message": "Hello, World!"}

@app.get("/items/{item_id}")
def get_item(item_id: int, q: str = None):
    return {"item_id": item_id, "query": q}
```

---

## Line-by-Line Explanation

```python
app = FastAPI()
```
> Creates the application instance. This is the central object.

#task #bug 

#task #bug 
#task 
```python
@app.get("/")
def root():
```
> Registers a GET route at `/`. The function name does not matter, only the decorator path does.

---

## Parameters / Customization

| Parameter  | Type | Description              | Example         |
|------------|------|--------------------------|-----------------|
| `item_id`  | int  | Path parameter           | `/items/42`     |
| `q`        | str  | Optional query parameter | `?q=search`     |

---

## Test / Expected Output

```bash
uvicorn main:app --reload
curl http://127.0.0.1:8000/items/42?q=hello
```

```json
{"item_id": 42, "query": "hello"}
```

---

## Watch Out For

- `item_id: int` — FastAPI validates the type. Passing a string returns a 422 error automatically.
- Always run with `uvicorn`, not plain `python main.py`

---

## Connections

- Theory: [[03_Knowledge/Example-Topic/Example-Topic]] — _To understand routing_
- Used in Project: [[02_Projects/Example-Project/Example-Project]]
- Similar Snippet: [[]]

---

## Tasks

- [x] #task Test it [due:: 2026-01-01]
- [x] #task Link to theory note [due:: 2026-01-01]
- [ ] #task Add authentication example
