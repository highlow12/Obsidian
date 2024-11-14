### MoC in Project & Area
```dataview
table
from "1. 프로젝트" OR "2. 에어리어" AND #MOC
sort file.cday DESC
limit 20
```
- - -

### Recent Coffee Review
```dataview
table date, rate
from "2. 에어리어/커피리뷰"
sort date DESC
limit 5
```
### Recent moded
```dataview
Table tags
FROM ""
SORT file.mtime DESC
LIMIT 5
```
### Clippings
```dataview
table source 
from "Clippings"
sort file.cday
```