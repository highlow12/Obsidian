- 탐색을 효율적으로 하기 위한 자료구조
- `KEY(왼쪽 서브 트리) <= KEY(루트노드) <= KEY(오른쪽 서브 트리)`
- 이진 탐색 트리를 [[Binary Tree Traversal#^ad56a4|중위순회]] 하면 오름차순으로 정렬된 값을 얻을 수 있다
# 탐색 알고리즘
```
search(node, key)
	if node == null return null
		
		if key == node.key return node
		
		else if key < node.key search(node.left, key)
		
		else search(node.right,key)
```
# 삽입 연산
- 삽입하기 위해 탐색을 해야 함
- **탐색에 실패한 위치**가 ==새로운 노드를 삽입하는 위치==
# 삭제 연산
- 단말 노드
	- 부모노드를 차아 연결을 끊는다
- 서브 트리중 하나만 가지고 있는 경우
	- 노드를 삭제하고 자식 노드를 부모 노드에 붙인다
- 2개의 서브트리를 모두 가지고 있는 경우