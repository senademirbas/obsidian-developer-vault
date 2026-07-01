---
kanban-plugin: basic
tags: [kanban, project]
---

## Backlog

- [ ] Requirements analysis
- [ ] Read documentation
- [ ] Environment setup

## This Sprint

- [ ] Build the core structure

## 🟡 In Progress

- [ ] Task being worked on

## Review

- [ ] Task to be reviewed

## Done

- [x] Project started

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
