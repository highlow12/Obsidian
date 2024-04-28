# 특징
1. 장점:
	- **데이터 참조가 쉽다**: 인덱스 값을 기준으로 어디든 한 번에 참조할 수 있습니다.
	- **구현이 쉽다**: 배열을 기반으로 구현되므로 비교적 간단합니다.
1. 단점:
	- **배열의 길이가 초기에 결정되어야 한다**: 배열 크기를 예측하여 넉넉하게 할당해야 하므로 메모리 낭비가 발생할 수 있습니다.
	- **삭제 과정에서 데이터 이동 (복사)가 빈번히 발생한다**: 삭제 시 데이터를 이동해야 하므로 효율성이 떨어집니다
# 구현
## isFull
```
function isFull(A, size):
    return size == length(A)
```
## isEmpty
```
function isEmpty(size):
    return size == 0
```
## insertElement
```
function insertElement(A, size, index, element):
    if isFull(A, size):
        print "List is full"
    else if index < 0 or index > size:
        print "Index out of bounds"
    else:
        for i from size down to index + 1:
            A[i] = A[i - 1]
        A[index] = element
        size = size + 1
```
## deletElement
```
function deleteElement(A, size, index):
    if isEmpty(size):
        print "List is empty"
    else if index < 0 or index >= size:
        print "Index out of bounds"
    else:
        for i from index to size - 2:
            A[i] = A[i + 1]
        size = size - 1
```
## getElement
```
function getElement(A, size, index):
    if index < 0 or index >= size:
        print "Index out of bounds"
    else:
        return A[index]
```
