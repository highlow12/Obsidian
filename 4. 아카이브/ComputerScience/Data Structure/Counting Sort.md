---
tags:
  - programming/Algorythem/Sort
---
### [[빅-오 표기법|시간복잡도]]
- 시간복잡도: O(n + k)
    - n: 정렬할 배열의 원소 개수
    - k: 배열의 최대값

### 공간복잡도
- 공간복잡도: O(n + k)
    - 카운트 배열: k 크기
    - 결과 배열: n 크기

### 작동 원리 및 특징
1. 정수 범위가 작은 경우에 매우 효율적인 정렬 알고리즘
2. 비교 기반 정렬 알고리즘이 아닌 분포 기반 정렬 알고리즘
3. 원소의 값을 직접 인덱스로 사용하여 정렬
> [!example]+ 
> ``` python
> def counting_sort(arr):
>     # 최대값 찾기
>     max_val = max(arr)
>     
>     # 카운트 배열 생성 및 초기화
>     count = [0] * (max_val + 1)
>     
>     # 각 원소의 등장 횟수 카운트
>     for num in arr:
>         count[num] += 1
>     
>     # 누적 카운트 계산
>     for i in range(1, len(count)):
>         count[i] += count[i-1]
>     
>     # 결과 배열 생성
>     output = [0] * len(arr)
>     
>     # 정렬된 결과 배열 만들기
>     for num in reversed(arr):
>         output[count[num] - 1] = num
>         count[num] -= 1
>     
>     return output
> ```