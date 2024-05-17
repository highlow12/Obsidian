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
- ![[이진 트리 순회.png|right|300]]
- 전위순회: VLR
	- 자손 노드보다 루트 노드를 먼저 방문한다
		- 예: 구조화된 문서 출력
- 중위순회: LVR ^ad56a4
	- 왼쪽 자손, 루트, 오른쪽 자손 순서대로 방문한다
		- 예: 수식 트리
- 후위순회: LRV
	- 루트노드 보다 자손 노드를 먼저 방문한다.
		- 예: 디렉터리 용량 계산
## 기본 순회 방법 알고리즘
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
# 트리의 레벨 순회
- 레벨 순회(Level order)는 각 노드를 레벨 순으로 검사하는 순회 방법
- 레벨 순회는 ==큐==를 사용한다
![[이진 트리 레벨 순회.png]]
## 레벨 순회 알고리즘
```
level_order(root):
	init Queue q
	q.enqueue(root)
	
	while is_empty(q):
		x = q.dequeue
		
		if x != null
			print(DATA(x))
			
		q.enqueue(Left(x))
		q.enqueue(Right(x))
```
# 이진 탐색 트리
![[Binary Search Tree]]