---
created: 2026-01-01
modified: 2026-07-02
type: snippet
status: 🔴 Baslanmadi
language: Python
domain: backend
dependencies:
  - fastapi
  - uvicorn
related_theory:
  - "[[03_Knowledge/Ornek-Konu/Ornek-Konu]]"
related_snippets: []
used_in_projects:
  - "[[02_Projects/Ornek-Proje/Ornek-Proje]]"
---

# FastAPI-Baslangic

> [!summary] Ne Yapar?
> Tek bir GET endpoint'i olan minimal FastAPI uygulamasi. Calistirabileceginiz en kucuk API.

**Bagli Teori:** [[03_Knowledge/Ornek-Konu/Ornek-Konu]]
**Kullanildigi Yer:** [[02_Projects/Ornek-Proje/Ornek-Proje]]

---

## Kod

```python
# ==================================================
# SNIPPET: FastAPI Baslangic
# Domain  : backend
# Dil     : Python
# Bagimli : fastapi, uvicorn
# ==================================================

from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def root():
    return {"message": "Merhaba, Dunya!"}

@app.get("/items/{item_id}")
def get_item(item_id: int, q: str = None):
    return {"item_id": item_id, "sorgu": q}
```

---

## Satir Satir Aciklama

```python
app = FastAPI()
```
> Uygulama orneginicreates eder. Bu merkezi nesnedir.

```python
@app.get("/")
def root():
```
> `/` yoluna GET rotasi kaydeder. Fonksiyon adinin onemi yoktur, yalnizca decorator yolu onemlidir.

---

## Parametreler / Ozellestirme

| Parametre  | Tip | Aciklama              | Ornek         |
|------------|-----|-----------------------|---------------|
| `item_id`  | int | Path parametresi      | `/items/42`   |
| `q`        | str | Opsiyonel query param | `?q=arama`    |

---

## Test / Beklenen Cikti

```bash
uvicorn main:app --reload
curl http://127.0.0.1:8000/items/42?q=merhaba
```

```json
{"item_id": 42, "sorgu": "merhaba"}
```

---

## Dikkat Edilecekler

- `item_id: int` — FastAPI tipi dogrular. String gecilmesi otomatik 422 hatasi doner.
- Her zaman `uvicorn` ile calistir, `python main.py` ile degil

---

## Baglantilar

- Teori: [[03_Knowledge/Ornek-Konu/Ornek-Konu]] — _Routing'i anlamak icin_
- Kullanildigi Proje: [[02_Projects/Ornek-Proje/Ornek-Proje]]
- Benzer Snippet: [[]]

---

## Yapilacaklar

- [x] #task Test et [due:: 2026-01-01]
- [x] #task Teori notuna link ver [due:: 2026-01-01]
- [ ] #task Kimlik dogrulama ornegi ekle
