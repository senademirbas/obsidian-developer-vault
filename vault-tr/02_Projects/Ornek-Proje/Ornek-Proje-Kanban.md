---
kanban-plugin: basic
tags: [kanban, project]
---

## Backlog

- [ ] Birim testleri yaz
- [ ] Kimlik dogrulama ekle
- [ ] CI/CD pipeline kur
- [ ] API dokumantasyonu yaz

## Bu Sprint

- [ ] POST /items endpoint olustur
- [ ] Veritabani baglantisi ekle

## 🟡 Devam Ediyor

- [ ] GET /items endpoint @{2026-01-15}

## Inceleme

- [ ] Proje iskeleti incelemesi

## Tamamlandi

- [x] Proje baslat
- [x] FastAPI kuruldu
- [x] Ana router yapisi olusturuldu

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
  "metadata-keys": [{"metadataKey": "due", "label": "", "shouldHideLabel": true, "containsMarkdown": false}]
}
```
%%
