---
tags:
  - List
  - DataStructure
  - Linear
---
# 원형 큐 ADT
`enqueue`: 큐의 뒤쪽에 항목을 추가합니다.
`dequeue`: 큐의 앞쪽에서 항목을 제거하고 반환합니다.
`front`: 큐의 맨 앞에 있는 항목을 제거하지 않고 반환합니다.
`rear`: 큐의 맨 뒤에 있는 항목을 제거하지 않고 반환합니다.
`isEmpty`: 큐가 비어 있는지 확인합니다.
`isFull`: 큐가 가득 찼는지 확인합니다.
`size`: 큐에 있는 항목의 수를 반환합니다.
# 구현
## enqueue 함수
```
function enqueue(item):
    if isFull() then
        return "Queue is full"
    end if
    rear = (rear + 1) % capacity
    queue[rear] = item
    size = size + 1
```
## dequeue 함수
```
function dequeue():
    if isEmpty() then
        return "Queue is empty"
    end if
    item = queue[front]
    front = (front + 1) % capacity
    size = size - 1
    return item
```
## front 함수
```
function front():
    if isEmpty() then
        return "Queue is empty"
    end if
    return queue[front]
```
## rear 함수
```
function rear():
    if isEmpty() then
        return "Queue is empty"
    end if
    return queue[rear]
```
## isEmpty 함수
```
function isEmpty():
    return size == 0
```
## isFull 함수
```
function isFull():
    return size == capacity
```