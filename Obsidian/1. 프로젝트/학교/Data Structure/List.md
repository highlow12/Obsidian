리스트는 순서가 있는 요소들의 집합을 모델링하는 기본적이고 범용적인 데이터 구조입니다. 리스트는 데이터를 순서대로 저장하고 접근할 수 있는 기능을 제공합니다.
용도: 투두 리스트, 버킷리스트 
# 리스트(List) Adt
- `insert(list, pos, item)`:  pos 위치에 요소를 추가한다.
- `insert_last(list, item)`:  맨 끝에 요소를 추가한다.
- `insert_first(list, item)`:  맨 처음에 요소를 추가한다.
- `delete(list, pos)`:  pos 위치의 요소를 제거한다.
- `clear(list)`:  리스트의 모든 요소를 제거한다.
- `get_entry(list, pos)`:  pos 위치의 요소를 반환한다.
- `get_length(list)`:  리스트의 길이를 구한다.
- `is_empty(list)`:  리스트가 비었는지를 검사한다.
- `is_full(list)`:  리스트가 꽉 찼는지를 검사한다.
- `print_list(list)`:  리스트의 모든 요소를 표시한다.
# 리스트 구현
![[배열 기반 리스트 구현]]
- - -
![[연결 리스트]]