---
subject: DataStructure
tags:
  - Algorythem/Search
  - DataStructure
  - DataStructure/Tree
---
AVL 트리(AVL Tree)는 [[Balanced Binary Search Tree|균형 이진 탐색 트리]]의 한 종류로, 균형을 유지하기 위해 회전 연산을 사용하는 자기-균형 [[Binary Search Tree]]입니다.

## AVL 트리의 특징
1. 균형 조건: AVL 트리의 각 노드는 왼쪽 서브트리와 오른쪽 서브트리의 *높이 차이가 1 이하*여야 합니다.
2. 자기-균형: AVL 트리는 삽입이나 삭제 연산 시 **균형을 자동으로 유지**합니다.
3. 시간 복잡도: AVL 트리의 탐색, 삽입, 삭제 연산은 ==모두 [[빅-오 표기법|O(log n)]]의 시간 복잡도==를 가집니다.

## AVL 트리의 균형 유지를 위한 회전 연산
1. 단순 회전(Single Rotation)
   - 왼쪽 회전: 오른쪽 편향된 트리를 균형 잡기 위해 왼쪽으로 회전
   - 오른쪽 회전: 왼쪽 편향된 트리를 균형 잡기 위해 오른쪽으로 회전
2. 이중 회전(Double Rotation)
   - 왼-오 회전: 오른-왼 편향된 트리를 균형 잡기 위해 왼쪽 회전 후 오른쪽 회전
   - 오-왼 회전: 왼-오 편향된 트리를 균형 잡기 위해 오른쪽 회전 후 왼쪽 회전

**AVL 트리의 삽입 연산 의사코드**
```
function AVL_insert(root, value):
    if root is null:
        return new Node(value)
    
    if value < root.value:
        root.left = insert(root.left, value)
    else if value > root.value:
        root.right = insert(root.right, value)
    else:
        return root # 중복된 값은 허용하지 않음
    
    root.height = 1 + max(height(root.left), height(root.right))
    
    balance = getBalance(root)
    
    
	# 4가지 회전 케이스 처리
    if balance > 1 and value < root.left.value:
        # 왼쪽 서브트리가 높고, 삽입된 값이 왼쪽 서브트리에 있는 경우
        # 오른쪽 회전을 수행하여 트리의 균형을 맞춤
        return rightRotate(root)
        
    if balance < -1 and value > root.right.value:
        # 오른쪽 서브트리가 높고, 삽입된 값이 오른쪽 서브트리에 있는 경우
        # 왼쪽 회전을 수행하여 트리의 균형을 맞춤
        return leftRotate(root)
        
    if balance > 1 and value > root.left.value:
        # 왼쪽 서브트리가 높고, 삽입된 값이 오른쪽 서브트리에 있는 경우
        # 먼저 왼쪽 서브트리에 대해 왼쪽 회전을 수행한 후,
        # 전체 트리에 대해 오른쪽 회전을 수행하여 균형을 맞춤
        root.left = leftRotate(root.left)
        return rightRotate(root)
        
    if balance < -1 and value < root.right.value:
        # 오른쪽 서브트리가 높고, 삽입된 값이 왼쪽 서브트리에 있는 경우
        # 먼저 오른쪽 서브트리에 대해 오른쪽 회전을 수행한 후,
        # 전체 트리에 대해 왼쪽 회전을 수행하여 균형을 맞춤
        root.right = rightRotate(root.right)
        return leftRotate(root)
    
    return root
```
![[AVL 트리의 삽입연산.png]]