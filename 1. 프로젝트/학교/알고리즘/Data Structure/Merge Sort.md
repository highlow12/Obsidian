---
tags:
  - programming/Algorythem
  - programming/Algorythem/Sort
subject: DataStructure
aliases:
  - 머지 소트
---
합병 정렬(Merge Sort)은 분할 정복 [[알고리즘]]의 대표적인 예로, 배열을 반으로 나누어 각각 정렬한 뒤 합치는 방식으로 정렬을 수행합니다.

합병 정렬의 작동 원리는 다음과 같습니다:

1. 배열을 반으로 나눕니다.
2. 나눠진 각 부분 배열을 재귀적으로 정렬합니다.
3. 정렬된 두 부분 배열을 합병하여 하나의 정렬된 배열을 만듭니다.

합병 정렬의 의사코드는 다음과 같습니다:

```
MergeSort(A)
    if length(A) <= 1
        return A
    
    mid = length(A) / 2
    left = A[0:mid]
    right = A[mid:]
    
    left = MergeSort(left)
    right = MergeSort(right)
    
    return Merge(left, right)

Merge(left, right)
    result = []
    i = 0
    j = 0
    
    while i < length(left) and j < length(right)
        if left[i] <= right[j]
            result.append(left[i])
            i = i + 1
        else
            result.append(right[j])
            j = j + 1
    
    while i < length(left)
        result.append(left[i])
        i = i + 1
    
    while j < length(right)
        result.append(right[j])
        j = j + 1
    
    return result
```

위의 의사코드를 설명하면 다음과 같습니다:

1. `MergeSort` 함수:
   - 배열의 길이가 `1` 이하이면 그대로 반환합니다.
   - 배열을 중간 지점을 기준으로 `left`와 `right` 부분 배열로 나눕니다.
   - `left`와 `right` 부분 배열을 각각 재귀적으로 `MergeSort` 함수를 호출하여 정렬합니다.
   - 정렬된 `left`와 `right` 부분 배열을 `Merge` 함수를 호출하여 합병합니다.

2. `Merge` 함수:
   - `left`와 `right` 부분 배열을 비교하면서 더 작은 값을 `result` 배열에 추가합니다.
   - `left` 또는 `right` 부분 배열에 남은 요소가 있다면 `result` 배열에 추가합니다.
   - 합병된 `result` 배열을 반환합니다.

합병 정렬은 분할 정복 방식을 사용하여 평균 시간 복잡도가 [[빅-오 표기법|O(n log n)]]으로, 매우 효율적인 정렬 알고리즘입니다. 하지만 추가적인 메모리 공간이 필요하다는 단점이 있습니다. 
![[합병 정렬.png]]