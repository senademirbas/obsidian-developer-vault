---
created: 2026-01-01
modified: 2026-07-02
type: knowledge
status: 🟡 Ogreniliyor
tags:
  - backend/fastapi/routing
parent: "[[Backend]]"
children:
  - "[[Bagimlilik Enjeksiyonu]]"
  - "[[FastAPI Middleware]]"
related_theory:
  - "[[Pydantic Modelleri]]"
related_snippets:
  - "[[04_Snippets/FastAPI-Baslangic]]"
related_projects:
  - "[[02_Projects/Ornek-Proje/Ornek-Proje]]"
source: https://fastapi.tiangolo.com/tutorial/
---

# Ornek-Konu

> [!abstract] Tek Cumle
> FastAPI routing, Python decorator'lari kullanarak URL endpoint'lerini tanimlar; path parametreleri, query string'leri ve otomatik OpenAPI uretimini destekler.

---

## Teori

### Ne?
FastAPI routing, HTTP metodlarini ve URL yollarini "path operation" denilen Python fonksiyonlarina esler.

### Neden?
Istek islemeyi is mantigından ayirir. Her rota temiz, tipli bir fonksiyondur.

### Nasil Calisir?
1. FastAPI uygulama ornegi olustur
2. Fonksiyonlarda decorator kullan (`@app.get`, `@app.post`, vb.)
3. FastAPI OpenAPI dokumantasyonunu otomatik uretir
4. Pydantic modelleri istek/yanit govdelerini dogrular

### Ne Zaman Kullanilir?
HTTP API gostermek istediginde. Async destek veya otomatik dogrulama gerektiginde Flask'a tercih et.

---

## Kritik Noktalar

- Path parametreleri: `@app.get("/items/{item_id}")`
- Query parametreleri: varsayilanli fonksiyon argumanlari olarak tanimlanir
- Yanit modelleri: otomatik serializasyon icin `response_model=` kullan
- Router'lar: buyuk API'leri modullere bolmek icin `APIRouter` kullan

---

## Parametreler / Konfigurasyon

| Parametre      | Aciklama                       | Default | Notum              |
|----------------|--------------------------------|---------|--------------------|
| `prefix`       | Router URL on eki              | ""      | ornegin `/api/v1`  |
| `tags`         | OpenAPI gruplama               | []      | /docs'ta gorunur   |
| `dependencies` | Paylasilan bagimlilik enjeksiyonu | []   | Auth, DB session   |

---

## Minimal Ornek

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/items/{item_id}")
def read_item(item_id: int, q: str = None):
    return {"item_id": item_id, "q": q}
```

> [!note] Cikari m
> FastAPI, fonksiyon imzalarindan tipleri cikarir. Ayri bir sema tanimi gerekmez.

---

## Baglantilar

**Teorik agac:**
- Ust konu → [[Backend]]
- Alt konular → [[Bagimlilik Enjeksiyonu]], [[FastAPI Middleware]]
- Karsilastir → [[Flask Routing]]

**Pratik:**
- Snippet → [[04_Snippets/FastAPI-Baslangic]]
- Proje → [[02_Projects/Ornek-Proje/Ornek-Proje]]

---

## Yapilacaklar

- [x] #task Kavrami bir ornekle uygula [due:: 2026-01-05]
- [ ] #task Middleware snippet yaz [due:: 2026-01-15]
- [ ] #task `children` alanini doldur [due:: 2026-01-10]
- [ ] #task Status'u guncelle

---

## Ham Notlar

_Henuz netlesmemis sorular._

- ? FastAPI versiyonlamay temiz nasil yapar?
- ? Paylasilan veritabani session'lari icin en iyi pattern ne?
