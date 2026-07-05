---
kanban-plugin: basic
tags: [kanban, project]
---

## Backlog

- [ ] Write unit tests
- [ ] Add authentication
- [ ] Set up CI/CD pipeline
- [ ] Write API documentation

## This Sprint

- [ ] Build POST /items endpoint
- [ ] Add database connection

## 🟡 In Progress

- [ ] GET /items endpoint @{2026-01-15}

## Review

- [ ] Project scaffold review

## Done

- [x] Project initialized
- [x] FastAPI installed
- [x] Main router structure created

%% kanban:settings
```
{
  "kanban-plugin": "basic",
  "list-collapse": [false, false, false, false, false],
  "date-trigger": "@",
  "date-format": "YYYY-MM-DD",
  "date-display-format": "YYYY-MM-DD",
  "show-checkboxes": true,
  "new-card-insertion-method": "prepend-compact",
  "lane-width": 270,
  "show-archive-all-button": true,
  "inline-metadata-position": "body",
  "move-tags-to-footer": true,
  "metadata-keys": [
    {
      "metadataKey": "due",
      "label": "",
      "shouldHideLabel": true,
      "containsMarkdown": false
    }
  ]
}
```
%%
