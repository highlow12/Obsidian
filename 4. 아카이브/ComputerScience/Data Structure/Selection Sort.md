---
subject: DataStructure
tags:
  - programming/Algorythem
  - programming/Algorythem/Sort
---
선택 정렬(Selection Sort)은 정렬 [[알고리즘]] 중 하나로, 배열의 모든 요소를 순차적으로 검사하여 가장 작은 값의 요소를 찾아 해당 위치에 배치하는 방식으로 정렬하는 알고리즘입니다.

선택 정렬의 작동 원리는 다음과 같습니다:

1. 주어진 배열에서 가장 작은 값의 요소를 찾습니다.
2. 찾은 가장 작은 값의 요소를 배열의 맨 앞 위치와 교환합니다.
3. 맨 앞 위치를 제외한 나머지 부분에 대해 위의 과정을 반복합니다.

선택 정렬의 의사코드는 다음과 같습니다:

```
SelectionSort(A)
    n = length(A)
    for i = 0 to n-2
        minIndex = i
        for j = i+1 to n-1
            if A[j] < A[minIndex]
                minIndex = j
        swap A[i] and A[minIndex]
    return A
```

위의 의사코드를 설명하면 다음과 같습니다:

1. 배열 `A`의 길이를 `n`으로 설정합니다.
2. `0`부터 `n-2`까지 반복하면서 다음을 수행합니다:
   - `minIndex` 변수를 `i`로 설정합니다.
   - i+1부터 n-1까지 반복하면서 다음을 수행합니다:
     - `A[j]`가 `A[minIndex]`보다 작으면 `minIndex`를 `j`로 설정합니다.
   - `A[i]`와 `A[minIndex]`의 값을 교환합니다.
3. 정렬된 배열 `A`를 반환합니다.

선택 정렬은 구현이 간단하지만, 시간 복잡도가 [[빅-오 표기법|O(n^2)]]으로 크지 않은 데이터 세트에 적합합니다. 하지만 더 효율적인 정렬 알고리즘(예: [[Quick Sort|퀵 정렬]], [[Merge Sort|병합 정렬]] 등)이 있기 때문에, 실제 사용에는 잘 사용되지 않습니다. 
