

### MoC
```dataview
table
tags
from "1. 프로젝트" OR "2. 에어리어" AND #MOC
```
- - -

### Recent Coffee Review
```dataview
table date, rate
from "2. 에어리어/커피리뷰"
sort date DESC
limit 5
```
### 할일
```todoist
name: 이번주 할일
filter: "due before: next week"
```
```todoist
name: 모든 할일
filter: "View all"
```