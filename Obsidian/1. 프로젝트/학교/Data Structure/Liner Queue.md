# 선형 큐 ADT
`create(max_size)`: 최대 크기가 max_size인 공백큐를 생성한다.
`init(q)`: 큐를 초기화한다.
`is_empty(q)`: if(size == 0) return TRUE; else return FALSE;
`is_full(q)`: if(size == max_size) return TRUE; else return FALSE;
`enqueue(q, e)`: if( is_full(q) ) queue_full 오류; else q의 끝에 e를 추가한다.
`dequeue(q)`: if( is_empty(q) ) queue_empty 오류; else q의 맨 앞에 있는 e를 제거하여 반환한다.
`peek(q)`: if( is_empty(q) ) queue_empty 오류; else q의 맨 앞에 있는 e를 읽어서 반환한다.
# 구현
## push 함수
```
function push(item):
    stack.append(item)
    size = size + 1
```

## pop 함수
```
function pop():
    if isEmpty() then
        return "Stack is empty"
    end if
    item = stack[size - 1]
    stack.remove(item)
    size = size - 1
    return item
```

## peek/top 함수
```
function peek():
    if isEmpty() then
        return "Stack is empty"
    end if
    return stack[size - 1]
```

## isEmpty 함수
```
function isEmpty():
    return size == 0
```