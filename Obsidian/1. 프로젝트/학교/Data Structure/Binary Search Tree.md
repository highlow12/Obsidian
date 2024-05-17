- 탐색을 효율적으로 하기 위한 자료구조
- `KEY(왼쪽 서브 트리) <= KEY(루트노드) <= KEY(오른쪽 서브 트리)`
- 이진 탐색 트리를 [[Binary Tree Traversal#^ad56a4|중위순회]] 하면 오름차순으로 정렬된 값을 얻을 수 있다
# 알고리즘
```
search(node, key)
	if node == null
		return null
		
		if key == node.key
			return node
		else if key < node.key
			search(node.left)
```