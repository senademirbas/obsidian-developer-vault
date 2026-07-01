---
tags:
  - daily
<%*
let d = moment(tp.file.title, "YYYY-MM-DD");
if (!d.isValid()){
    tR += "date: \"" + tp.file.title + "\"\n";
} else {
    tR += "date: " + d.format("YYYY-MM-DD") + "\n";
    tR += "week: \"[[" + d.format("gggg-[W]ww") + "]]\"\n";
    let prev, next;
    if (d.isoWeekday() === 1) {
        prev = moment(d).subtract(3, "days");
    } else {
        prev = moment(d).subtract(1, "days");
    }
    if (d.isoWeekday() === 5) {
        next = moment(d).add(3, "days");
    } else {
        next = moment(d).add(1, "days");
    }
    tR += "prev: \"[[01_Daily/" + prev.format("YYYY-MM-DD") + "]]\"\n";
    tR += "next: \"[[01_Daily/" + next.format("YYYY-MM-DD") + "]]\"\n";
}
tR += "type: daily\n";
%>
---

# <% tp.file.title %>

## Gunun Odagi

_Bugun en onemli olan tek sey ne?_

---

## Gorevler
> Gorev eklemek icin `Ctrl+X` kullan — aciklamayi yaz, Enter'a bas, tarih sec.
> Kanban tablolarinda `+` butonunu ve tarih icin `@{}` yapisini kullan.

- [ ] #task gorev aciklamasi [due:: <% tp.date.now("YYYY-MM-DD") %>]
- [ ] #task gorev aciklamasi [due:: <% tp.date.now("YYYY-MM-DD") %>]

---

## Zaman Bloklari

| Zaman | Plan | Durum |
|-------|------|-------|
| 09:00 |      | [ ]   |
| 11:00 |      | [ ]   |
| 14:00 |      | [ ]   |
| 16:00 |      | [ ]   |
| 19:00 |      | [ ]   |

---

## Notlar

_

---

## Kod / Fikirler

```python

```

---

## Gunun Ozeti

_Ne yaptim? Yarin ne devam edecek?_
