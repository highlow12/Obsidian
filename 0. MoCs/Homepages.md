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
LIMIT 10
```
### Clippings
```dataview
table source, published, description
from "Clippings"
sort file.cday
```
### All MoCs
```dataview
table file.path, file.mday
from #MOC
sort file.mday DESC
```