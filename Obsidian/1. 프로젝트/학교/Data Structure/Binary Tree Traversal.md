---
tags:
  - "#Tree"
  - DataStructure
  - Non-Linear
  - Traversal
  - Algorythem
---
***순회(Traversal)***: 트리의 노드들을 쳬계적으로 방문 하는 것
# 기본적인 순회 방법
- ![[Pasted image 20240513165657.png|right|300]]
- 전위순회: VLR
	- 자손 노드보다 루트 노드를 먼저 방문한다
- 중위순회:LVR
	- 왼쪽 자손, 루트, 오른쪽 자손 순서대로 방문한다
- 후위순회: LRV
	- 루트노드 보다 자손 노드를 먼저 방문한다.
## 순회 방법 코드
### 전위순회
```
preorder(x):
	if x != null:
		print DATA(X)
		preorder(Left(x))
		Preorder(Right(x))
```