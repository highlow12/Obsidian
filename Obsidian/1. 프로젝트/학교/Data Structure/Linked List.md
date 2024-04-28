# 특징
1. 장점:
    - **데이터의 삽입과 삭제가 쉽다**: 연결 리스트는 링크로써 구현되기 때문에 자료의 삽입 및 삭제가 용이합니다.
    - **크기가 가변적이다**: 배열과 달리 중간에 요소를 삽입하거나 삭제하는 비용이 적습니다.
2. 단점:
    - **원하는 원소를 찾는 과정에서 탐색 비용이 높다**: 데이터를 찾기 위해 포인터로 모든 노드를 순회해야 하므로 탐색 속도가 느립니다.
    - **구현이 어렵다**: 배열에 비해 구현이 복잡할 수 있습니다
# **개념정리**: 중요!
1. 노드(주소 값, data 값, link 값)
	1. new: 노드의 주소
	2. new -> data: new 노드의 데이터 필드값
	3. new -> link: new의 link 필드값 (== new.link)
2. head porinter(head (== \*phead)
	1. head: 첫번째 노드의 주소 값
3. pre/p pointer (= 배열에서 index와 같은 역할)
	1. pre/p pointer: 삽입될 노드의 선행 포인터.
# 구현
## 노드
```
Node:
    element
    next
```
## creatList
```
function createList():
    head = null
    return head
```
## insert
```
function insert(head, pre, element):
	newnode = new node
	newnode.element = element
	newnode.next = pre.next
	pre.next = newnode
	return head
```
## isEmpty
```
function isEmpty(head):
    return head == null
```
## insertAtBeginning
```
function insertAtBeginning(head, element):
    newNode = new Node
    newNode.element = element
    newNode.next = head
    head = newNode
    return head
```
## insertAtEnd
```
function insertAtEnd(head, element):
    newNode = new Node
    newNode.element = element
    newNode.next = null
    if isEmpty(head):
        head = newNode
    else:
        current = head
        while current.next != null:
            current = current.next
        current.next = newNode
    return head
```
## deleteFromBeginning
```
function deleteFromBeginning(head):
    if isEmpty(head):
        print "List is empty"
    else:
        head = head.next
    return head
```
## deletFromEnd
```
function deleteFromEnd(head):
    if isEmpty(head):
        print "List is empty"
    elif head.next == null:
        head = null
    else:
        current = head
        while current.next.next != null:
            current = current.next
        current.next = null
    return head
```
## findElement
```
function findElement(head, element):
    position = 0
    current = head
    while current != null:
        if current.element == element:
            return position
        current = current.next
        position += 1
    return -1  // 원소를 찾지 못했을 때
```
# 원형 연결 리스트
![[Circular Linked List]]
# 이중 연결 리스트
![[Doubly Linked List]]