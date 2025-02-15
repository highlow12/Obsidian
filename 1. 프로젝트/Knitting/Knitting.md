---
tags:
  - MOC
  - Knitting
  - Crochet
---

## 시작 날짜

```dataview
LIST Start date
FROM "프로젝트/Knitting"
WHERE contains(file.name, "Note") AND Start date
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

## 바늘/코바늘

```dataview
LIST Niddle/Hook
FROM "프로젝트/Knitting"
WHERE contains(file.name, "Note") AND Niddle/Hook
SORT file.mtime desc
```

## 게이지

```dataview
LIST Gauge
FROM "프로젝트/Knitting"
WHERE contains(file.name, "Note") AND Gauge
SORT file.mtime desc
```

## 패턴

```dataview
LIST Pattern
FROM "프로젝트/Knitting"
WHERE contains(file.name, "Note") AND Pattern
SORT file.mtime desc
```