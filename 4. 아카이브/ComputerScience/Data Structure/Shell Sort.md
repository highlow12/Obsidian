---
subject: DataStructure
tags:
  - programming/Algorythem
  - programming/Algorythem/Sort
aliases:
  - 쉘 정렬
---
셸 정렬(Shell Sort)은 [[Selection Sort|삽입 정렬]]을 개선한 정렬 [[알고리즘]]입니다. 셸 정렬은 삽입 정렬의 단점을 보완하여 더 빠른 정렬 속도를 제공합니다.

셸 정렬의 작동 원리는 다음과 같습니다:

1. 배열을 일정한 간격(gap)으로 나누어 부분 정렬을 수행합니다.
2. 반복적으로 gap을 줄이면서 부분 정렬을 수행합니다.
3. gap이 1이 되면 일반적인 삽입 정렬을 수행하여 최종 정렬을 완성합니다.

셸 정렬의 의사코드는 다음과 같습니다:

```
ShellSort(A)
    n = length(A)
    gap = n / 2
    while gap > 0
        for i = gap to n-1
            temp = A[i]
            j = i
            while j >= gap and A[j-gap] > temp
                A[j] = A[j-gap]
                j = j - gap
            A[j] = temp
        gap = gap / 2
    return A
```

위의 의사코드를 설명하면 다음과 같습니다:

1. 배열 `A`의 길이를 `n`으로 설정합니다.
2. 초기 `gap`을 `n/2`로 설정합니다.
3. `gap`이 `0`보다 클 때까지 다음을 반복합니다:
   - `gap`부터 `n-1`까지 반복하면서 다음을 수행합니다:
     - `A[i]`를 `temp`에 저장합니다.
     - `j`를 `i`로 설정합니다.
     - `j`가 `gap` 이상이고 `A[j-gap]`이 `temp`보다 크면 다음을 수행합니다:
       - `A[j]`에 `A[j-gap]`을 대입합니다.
       - `j`를 `j-gap`으로 업데이트합니다.
     - `A[j]`에 `temp`를 대입합니다.
   - `gap`을 `gap/2`로 업데이트합니다.
4. 정렬된 배열 `A`를 반환합니다.

셸 정렬은 삽입 정렬을 개선한 알고리즘으로, **간격을 줄여가며 ==부분 정렬을 수행==하여 전체적인 정렬 속도를 향상시킵니다.** 평균 시간 복잡도는 [[빅-오 표기법|O(n^(3/2))]]이지만, 실제 데이터에 따라 더 좋은 성능을 보일 수 있습니다. 또한 구현이 비교적 간단하여 교육용으로도 많이 사용됩니다. 