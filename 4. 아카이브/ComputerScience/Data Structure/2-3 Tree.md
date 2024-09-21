---
tags:
  - DataStructure
  - DataStructure/Tree
  - Algorythem/Search
---
2-3 트리는 2-3 검색 트리라고도 불리는 [[Balanced Binary Search Tree|자가 균형 이진 탐색 트리]]의 일종입니다. 
## 2-3 트리의 특징
1. 각 노드는 1개 또는 2개의 키를 가질 수 있습니다.
2. 각 노드는 최대 3개의 자식 노드를 가질 수 있습니다.
3. 모든 리프 노드는 같은 깊이를 가집니다.
4. 각 노드의 키는 오름차순으로 정렬되어 있습니다.

2-3 트리의 삽입, 삭제, 검색 연산의 시간 복잡도는 다음과 같습니다:

1. 삽입 (insert) 시간 복잡도: [[빅-오 표기법|O(log n)]]
   - 2-3 트리의 높이는 log n 이므로, 각 레벨에서 키를 찾아 내려가는 작업이 log n 시간이 소요됩니다.
   - 필요한 경우 노드 분할 작업이 추가로 수행되지만, 이 또한 log n 시간 내에 수행됩니다.

2. 삭제 (delete) 시간 복잡도: O(log n)
   - 삭제할 키를 찾아 내려가는 작업이 log n 시간이 소요됩니다.
   - 필요한 경우 노드 병합 및 재균형 작업이 추가로 수행되지만, 이 또한 log n 시간 내에 수행됩니다.

3. 검색 (search) 시간 복잡도: O(log n)
   - 2-3 트리의 높이가 log n 이므로, 각 레벨에서 키를 찾아 내려가는 작업이 log n 시간이 소요됩니다.

이와 같이 2-3 트리는 삽입, 삭제, 검색 모두 O(log n) 시간 복잡도를 가지므로, 균형 잡힌 이진 탐색 트리로 활용될 수 있습니다. 이는 자가 균형 기능으로 인해 트리의 높이가 항상 균형을 이루기 때문입니다. 

## 2-3 트리의 삽입, 삭제, 검색 연산의 과정
1. 삽입 (Insert) 연산:
   - 값을 삽입할 위치를 찾아 내려간다.
   - 리프 노드에 도달하면 해당 노드에 값을 삽입한다.
   - 노드에 키가 3개가 되면 중간 키를 상위 노드로 올리고, 나머지 키로 2개의 새로운 노드를 생성한다.
   - 상위 노드에서도 키가 3개가 되면 중간 키를 다시 상위 노드로 올리는 작업을 반복한다.
   - 루트 노드에서도 키가 3개가 되면 루트 노드를 분할하여 새로운 루트 노드를 생성한다.
2. 삭제 (Delete) 연산:
   - 삭제할 값을 찾아 내려간다.
   - 리프 노드에 도달하면 해당 값을 삭제한다.
   - 삭제 후 노드의 키 개수가 1개가 되면 인접 노드와 병합한다.
   - 병합 후에도 키 개수가 부족하면 상위 노드에서 키를 빌려온다.
   - 상위 노드에서도 키 개수가 부족하면 계속해서 상위 노드로 올라가며 재균형 작업을 수행한다.
3. 검색 (Search) 연산:
   - 찾고자 하는 값을 기준으로 노드의 키를 비교하며 내려간다.
   - 키 값이 일치하면 해당 노드를 반환한다.
   - 키 값이 일치하지 않으면 해당 키의 위치를 기준으로 왼쪽 또는 오른쪽 자식 노드로 내려간다.
   - 리프 노드에 도달했는데도 찾고자 하는 값이 없으면 해당 값이 트리에 없다는 것을 의미한다.

이와 같이 2-3 트리는 자가 균형 기능을 가지고 있어, 삽입/삭제/검색 연산 시 트리의 균형을 유지하며 효율적으로 동작할 수 있습니다. 이를 통해 시간 복잡도를 O(log n)으로 유지할 수 있습니다. 

**2-3 트리의 삽입, 삭제, 검색 연산 의사코드로 **
```
# 2-3 트리 노드 정의
class Node:
    def __init__(self, keys=[], children=[]):
        self.keys = keys
        self.children = children

# 2-3 트리 삽입 함수
def insert(root, value):
    if root is None:
        return Node([value])
    
    i = 0
    while i < len(root.keys) and value > root.keys[i]:
        i += 1
    
    if len(root.children) > 0:
        root.children[i] = insert(root.children[i], value)
    else:
        root.keys.insert(i, value)
        if len(root.keys) > 2:
            mid = root.keys.pop(1)
            left_keys = root.keys[:1]
            right_keys = root.keys[1:]
            left_child = Node(left_keys)
            right_child = Node(right_keys)
            root = Node([mid], [left_child, right_child])
    
    return root

# 2-3 트리 검색 함수
def search(root, value):
    if root is None:
        return False
    
    i = 0
    while i < len(root.keys) and value > root.keys[i]:
        i += 1
    
    if i < len(root.keys) and value == root.keys[i]:
        return True
    elif len(root.children) > 0:
        return search(root.children[i], value)
    else:
        return False

# 2-3 트리 삭제 함수
def delete(root, value):
    if root is None:
        return None
    
    i = 0
    while i < len(root.keys) and value > root.keys[i]:
        i += 1
    
    if i < len(root.keys) and value == root.keys[i]:
        if len(root.children) == 0:
            root.keys.pop(i)
        else:
            successor = find_successor(root.children[i+1])
            root.keys[i] = successor
            root.children[i+1] = delete(root.children[i+1], successor)
    else:
        root.children[i] = delete(root.children[i], value)
    
    if len(root.children) > 0 and len(root.keys) < 1:
        root = root.children[0]
    
    return root

# 후계자 찾기 함수
def find_successor(node):
    while len(node.children) > 0:
        node = node.children[0]
    return node.keys[0]
```

이 의사코드에서는 2-3 트리의 기본적인 삽입, 검색, 삭제 연산을 구현하고 있습니다. 삽입 시에는 노드의 키가 2개를 초과하면 중간 키를 분리하여 새로운 노드를 생성하고, 삭제 시에는 후계자를 찾아 대체하는 방식으로 구현되어 있습니다. 이를 통해 2-3 트리의 균형을 유지할 수 있습니다. 