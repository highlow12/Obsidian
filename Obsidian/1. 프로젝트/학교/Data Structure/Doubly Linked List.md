# 특징
1. 하나의 노드가 선행 노드와 후속 노드에 대한 두 개의 링크를 가지는 리스트
2. 공간을 많이 차지하고 코드가 복잡함
3. **head node** 존재
# 구현
## 노드
```
Dlnode:
	element
	Llink
	Rlink
```
## insert
```
function dinsert(node, pre, element):
	newnode = new node
	newnode.element = element
	
	newnode.Llink = pre
	newnode.Rlink = pre.Rlink
	
	pre.Rlink.Llink = newnode
	pre.Rlink = newnode
```
## remove
```
function ddlete(head, removed):
	if removed == head:
		return
	removed.Llink.Rlink = removed.Rlink
	removed.Rlink.Llink = removed.Llink
	
	free removed
```
