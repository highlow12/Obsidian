---
tags:
  - MOC
  - Knitting
  - Crochet
---

## 🐙문어발 개수

```dataviewjs
const today = new Date();
const notes = dv.pages('"프로젝트/Knitting"').where(p => p.file.name.includes("Note") && p["Start date"] && p["Start date"] <= today && !p["Done-date"]);
dv.paragraph("현재 문어발 개수: " + notes.length);
```

## 시작 날짜

```dataview
LIST Start-date
FROM "프로젝트/Knitting"
WHERE contains(file.name, "Note") AND Start-date
SORT file.mtime desc
```

## 완료 날짜

```dataview
LIST Done-date
FROM "프로젝트/Knitting"
WHERE contains(file.name, "Note") AND Done-date
SORT file.mtime desc
```

## 실

```dataview
LIST Yarn
FROM "프로젝트/Knitting"
WHERE contains(file.name, "Note") AND Yarn
SORT file.mtime desc
```

## 패턴

```dataview
LIST Pattern
FROM "프로젝트/Knitting"
WHERE contains(file.name, "Note") AND Pattern
SORT file.mtime desc
```


