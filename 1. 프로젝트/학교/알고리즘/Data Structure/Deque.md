덱(Deque, Double-Ended [[Queue]])은 양쪽 끝에서 삽입과 삭제가 가능한 자료구조입니다. 덱은 큐(Queue)와 스택([[Stack]])의 특성을 모두 갖고 있어, 다양한 방식으로 데이터를 처리할 수 있습니다. 아래는 덱의 주요 특징과 동작 방식에 대한 설명입니다.
### 주요 특징

1. **양쪽 끝에서의 접근**:
   - 덱은 앞(front)과 뒤(rear) 양쪽 끝에서 데이터를 삽입하거나 삭제할 수 있습니다. 이로 인해 더 유연한 데이터 처리가 가능합니다.

2. **FIFO와 LIFO의 혼합**:
   - 덱은 큐처럼 FIFO(First In First Out) 방식으로 데이터를 처리할 수 있지만, 스택처럼 LIFO(Last In First Out) 방식으로도 사용할 수 있습니다.

3. **동적 크기 조절**:
   - 배열 기반의 덱은 크기가 고정되어 있지만, [[Linked List|링크드 리스트]] 기반의 덱은 동적으로 크기를 조절할 수 있어 유연성이 높습니다.

4. **상수 시간 복잡도**:
   - 삽입과 삭제 연산이 양쪽 끝에서 이루어지므로, 평균적으로 [[빅-오 표기법|O(1)]]의 시간 복잡도로 빠르게 수행됩니다.

### 기본 연산

1. **삽입 연산**:
   - `insertFront(item)`: 앞쪽에 아이템을 추가합니다.
   - `insertRear(item)`: 뒤쪽에 아이템을 추가합니다.

2. **삭제 연산**:
   - `deleteFront()`: 앞쪽에서 아이템을 제거하고 반환합니다.
   - `deleteRear()`: 뒤쪽에서 아이템을 제거하고 반환합니다.

3. **조회 연산**:
   - `getFront()`: 앞쪽 아이템을 반환합니다 (삭제하지 않음).
   - `getRear()`: 뒤쪽 아이템을 반환합니다 (삭제하지 않음).

4. **체크 연산**:
   - `isEmpty()`: 덱이 비어 있는지 확인합니다.
   - `getSize()`: 덱에 있는 아이템의 개수를 반환합니다.

### 사용 사례

- **버퍼 관리**: 데이터 흐름을 관리할 때, 예를 들어 스트리밍 데이터 처리.
- **문자열 처리**: 문자열의 회문 검사와 같은 알고리즘.
- **탐색 알고리즘**: 너비 우선 탐색(BFS)에서 큐로 사용되거나, 특정 상황에서 스택으로 사용될 수 있습니다.

이러한 특징 덕분에 덱은 다양한 알고리즘과 데이터 처리에 유용하게 사용됩니다. 추가적인 질문이 있으면 말씀해 주세요! 
### 링크드 리스트를 이용한 덱 구현(수도코드)
> [!example]-
> ```sudo
> Class Node:
>     Attributes:
>         data
>         nextNode
>         prevNode
> 
> Class Deque:
>     Attributes:
>         frontNode
>         rearNode
>         size
> 
>     Methods:
>         Constructor:
>             frontNode = null
>             rearNode = null
>             size = 0
> 
>         insertFront(item):
>             newNode = new Node(item)
>             if frontNode is null:
>                 frontNode = newNode
>                 rearNode = newNode
>             else:
>                 newNode.nextNode = frontNode
>                 frontNode.prevNode = newNode
>                 frontNode = newNode
>             size += 1
> 
>         insertRear(item):
>             newNode = new Node(item)
>             if rearNode is null:
>                 frontNode = newNode
>                 rearNode = newNode
>             else:
>                 rearNode.nextNode = newNode
>                 newNode.prevNode = rearNode
>                 rearNode = newNode
>             size += 1
> 
>         deleteFront():
>             if frontNode is null:
>                 return null
>             nodeToDelete = frontNode
>             frontNode = frontNode.nextNode
>             if frontNode is null:
>                 rearNode = null
>             else:
>                 frontNode.prevNode = null
>             size -= 1
>             return nodeToDelete.data
> 
>         deleteRear():
>             if rearNode is null:
>                 return null
>             nodeToDelete = rearNode
>             rearNode = rearNode.prevNode
>             if rearNode is null:
>                 frontNode = null
>             else:
>                 rearNode.nextNode = null
>             size -= 1
>             return nodeToDelete.data
> 
>         getFront():
>             if frontNode is null:
>                 return null
>             return frontNode.data
> 
>         getRear():
>             if rearNode is null:
>                 return null
>             return rearNode.data
> 
>         isEmpty():
>             return size == 0
> 
>         getSize():
>             return size
> 
> ```