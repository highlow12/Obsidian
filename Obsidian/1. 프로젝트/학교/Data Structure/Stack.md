# 스택의 특징
1. ***[[LIFO|LIFO(Last in First out)]]***: 후입선출
# 스택 추상데이터 타입(ADT)
## 객체
- 0개 이상의 원소를 가지는 유한 선형 리스트
## 연산
- `creat(size)`: 최대 트기가 size인 스택을 만든다
- `is_full(stack)` : if(stack.원소수 == size) return True else False
- `is_empty(stack)`: if(stack.원소수 == 0) return True else False
- `push(stack, item)`: if(is_full(stack)) return ERROR_STACKFULL; else 스택의 맨 위에 item을 추가한다.
- `pop(stack)`: if(is_empty(stack)) return ERROR_STACKEMPTY; else 스택의 맨 위의 원소를 제거해서 반환한다.
- `peek(stack)`:if(is_empty(stack)) return ERROR_STACKEMPTY; else 스택의 맨 위의 원소를 제거하지 않고 반환한다.
# 구현
- 