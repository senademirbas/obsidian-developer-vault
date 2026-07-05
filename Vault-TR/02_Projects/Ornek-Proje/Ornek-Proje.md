---
created: 2026-01-01
modified: 2026-07-02
type: project
status: 🟡 Devam Ediyor
deadline: 2026-03-01
tags:
  - project
related_knowledge:
  - "[[03_Knowledge/Ornek-Konu/Ornek-Konu]]"
related_snippets:
  - "[[04_Snippets/FastAPI-Baslangic]]"
repo: https://github.com/kullaniciadi/ornek-proje
---


# Ornek-Proje

> [!abstract] Proje Ozeti
> Bu vault'un nasil kullanildigini gostermek icin FastAPI ile minimal bir REST API olusturuyoruz.

---
## Hedefler

- [x] #task Proje yapisini kur [due:: 2026-01-05]
- [x] #task Ilk endpoint'i olustur [due:: 2026-01-10]
- [ ] #task Testleri yaz [due:: 2026-01-20]
- [ ] #task Production'a deploy et [due:: 2026-03-01]

---
## Milestoneler

| Tarih      | Hedef                  | Durum |
| ---------- | ---------------------- | ----- |
| 2026-01-10 | Cekirdek API calisiyor | 🟢    |
| 2026-02-01 | Testler gecti          | 🔴    |
| 2026-03-01 | Production deploy      | 🔴    |

---

## Teknik Kararlar
_Neden Flask yerine FastAPI? FastAPI native async destegi ve otomatik OpenAPI dokumantasyonu sunuyor._

- Pydantic v2 secildi — daha siki tipler, daha iyi performans
- Gelistirme icin SQLite, production icin PostgreSQL

---

## Acik Sorular

- V1'de mi yoksa V2'de mi kimlik dogrulama ekleyelim?
- Hangi deploy platformu: Railway, Fly.io veya VPS?

---

## Baglantilar

- Ilgili Teori: [[03_Knowledge/Ornek-Konu/Ornek-Konu]]
- Ilgili Snippet: [[04_Snippets/FastAPI-Baslangic]]
- Repo / Link: https://github.com/kullaniciadi/ornek-proje

---

## Gunluk Ilerleme

### 2026-01-10
_Cekirdek API yapisi olusturuldu. GET /items endpoint calisiyor. Sirada POST var._

- Tamamlanan: proje iskeleti, main.py, router yapisi
- Engel: veritabani sema kararlari

### 2026-01-01
_Proje baslangic. FastAPI + SQLite stack'i kararlastirildi._

-
