---
tags:
  - DataStructure/List
  - DataStructure
  - DataStructure/Linear
---
# 특징
1. 마지막 노드가 첫번째 노드를 가리키는 리스트
2. 처음이나 끝에 노드를 삽입하는 연산이 다른 연결 리스트보더 효율적
3. 한 노드에서 다른 모든 노드로의 접근이 가능
# 구현
## insertAtBeginning
```
function insertAtBeginning(head, element):
	newnode = new node
	newnode.element = element
	
	if head == null:
		head = newnode
		node.next = head
	else:
		node.next = head.link
		head.next = newnode
		
	return head
```
## insertAtEnd
```
function insertAtEnd(head element):
	newnode = new node
	newNode.element = element
	
    if head == null:
	    head = node
	    node.next = head
	else:
		node.next = head.next
		head.next = node
		head = node
		
	return head;
```