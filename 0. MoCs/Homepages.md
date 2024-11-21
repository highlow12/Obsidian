## Coffee
### Recent Coffee Review
```dataview
table date, rate
from "2. 에어리어/커피리뷰"
sort date DESC
limit 5
```
#### 전체 커피 리뷰
[[커피리뷰 리스트]]
## MOC
### MoC in Project & Area
```dataview
table
from "1. 프로젝트" OR "2. 에어리어" AND #MOC
sort file.cday DESC
limit 20
```
> [!info]- All MoCs 
> ```dataview
> table file.path as "위치", file.mday as "마지막 수정"
> from #MOC
> sort file.mday DESC
> ```
## Recent Note
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

