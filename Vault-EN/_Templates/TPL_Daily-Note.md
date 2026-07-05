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

## Focus

_What is the one thing that matters most today?_

---

## Tasks
> Add a task with `Ctrl+X` — type description, press Enter, then pick a date.
> In Kanban boards, use the `+` button and `@{}` for dates instead.

- [ ] #task task description [due:: <% tp.date.now("YYYY-MM-DD") %>]
- [ ] #task task description [due:: <% tp.date.now("YYYY-MM-DD") %>]

---

## Time Blocks

| Time  | Plan | Status |
|-------|------|--------|
| 09:00 |      | [ ]    |
| 11:00 |      | [ ]    |
| 14:00 |      | [ ]    |
| 16:00 |      | [ ]    |
| 19:00 |      | [ ]    |

---

## Notes

_

---

## Code / Ideas

```python

```

---

## Summary

_What did I accomplish? What carries over to tomorrow?_
