---
subject: DataStructure
tags:
  - DataStructure
  - Non-Linear
---
# 사전
딕셔너리(Dictionary)는 키-값 쌍(key-value pair)을 저장하는 자료 구조입니다. 키는 고유한 식별자로 사용되며, 값은 키에 대응되는 데이터입니다. 딕셔너리는 빠른 검색, 삽입, 삭제 등의 연산을 제공하며, 이를 통해 효율적인 데이터 관리가 가능합니다.

딕셔너리의 ADT(Abstract Data Type) 의사코드는 다음과 같습니다:

```
ADT Dictionary:
    create_dictionary(): 새로운 딕셔너리를 생성하고 반환합니다.
    insert(dictionary, key, value): 딕셔너리에 새로운 키-값 쌍을 삽입합니다.
    delete(dictionary, key): 딕셔너리에서 특정 키에 해당하는 키-값 쌍을 삭제합니다.
    search(dictionary, key): 딕셔너리에서 특정 키에 해당하는 값을 반환합니다.
    is_empty(dictionary): 딕셔너리가 비어있는지 확인하고 결과를 반환합니다.
    size(dictionary): 딕셔너리에 저장된 키-값 쌍의 개수를 반환합니다.

function create_dictionary():
    새로운 딕셔너리 객체를 생성하고 반환한다.

function insert(dictionary, key, value):
    if dictionary.is_empty():
        dictionary[key] = value
    else:
        if key in dictionary:
            dictionary[key] = value
        else:
            dictionary[key] = value

function delete(dictionary, key):
    if key in dictionary:
        del dictionary[key]
    else:
        return error

function search(dictionary, key):
    if key in dictionary:
        return dictionary[key]
    else:
        return error

function is_empty(dictionary):
    if len(dictionary) == 0:
        return true
    else:
        return false

function size(dictionary):
    return len(dictionary)
```

이와 같이 딕셔너리는 키-값 쌍을 저장하고 관리하는 자료 구조로, 빠른 검색, 삽입, 삭제 등의 연산을 제공합니다. 이러한 특성 때문에 다양한 프로그래밍 언어에서 널리 사용되고 있습니다. 