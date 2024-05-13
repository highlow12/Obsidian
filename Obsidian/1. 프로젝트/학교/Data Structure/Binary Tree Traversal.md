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
		- 예: 구조화된 문서 출력
- 중위순회: LVR
	- 왼쪽 자손, 루트, 오른쪽 자손 순서대로 방문한다
		- 예: 수식 트리
- 후위순회: LRV
	- 루트노드 보다 자손 노드를 먼저 방문한다.
		- 예: 디렉터리 용량 계산
## 순회 방법 코드
### 전위순회
```
preorder(x):
	if x != null:
		print(DATA(X))
		preorder(Left(x))
		Preorder(Right(x))
```
### 중위 순회
```
inorder(x):
	if x != null:
		inorder((Left(x)))
		print(DATA(x))
		inorder(Right(x))
```
### 후위 순회
```
postorder(x):
	if x != null:
		postorder(Left(x))
		postorder(Right(x))
		print(DATA(X))
```