---
tags:
  - programming/Algorythem
  - 수정중
aliases:
  - 4 여왕말 문제
  - n 여왕말 문제
---
제약 충족 문제(CPS) 의 대표적인 예제
# 4 여왕말 문제
4 여왕말 문제는 1,2,3,4 네개의 여왕말이 4\*4 크기의 체스판에서 잡히지 않게 배치하는 문제
4 여왕말 문제를 정형화하면 다음과 같다
- 변수: 1부터 4까지 이름이 붙은 4개의 여왕말
- 도메인: 4\*4 모양의 체스판에 포함된 4개의 열
- 제약 조건: 서로 다른 두개의 여왕말이 하나의 행, 열, 대삭선 상에 존재하지 않음
![|200](https://raw.githubusercontent.com/codingalzi/algopy/master/jupyter-book/imgs/algo05/algo05-01a.png)
위는 앞서 언급된 제약 조건을 만족시키거나 아닌 경우를 보여준다
## 4 여왕말 문제 되추적 알고리즘
4개의 여왈말을 서로 공격하지 못하도록 배치하는 4 여왕말 문제를 해겨하는 되추적 알고리즘은 상태공간 트리를 대상으로 깊이 우선 탐색, 노드의 유망성 판단, 가지치기를 아래 과정에 따라 반복 실행한다
 - 4\*4로 이루어진 체스판에 네 개의 체스 여왕말을 놓을 수 있는 위치를 노드로 표현한 상태 공간 트리의 루트에서부터 깊이 우선 탐색을 실행
 - 탐색 과정에서 유망하지 않은 노드를 만나면 가지치기 실행 후 깊이 우선 탐색이 될수 있는 저삭 노드를 갖는 조상 노드로 되돌아가서,즉 ==되추적하여== 그곳에서부터 깊이 우선 탐색을 실행.
 - 탐색이 더 이상 진행될수 없는 경우 알고리즘 종료
<sub>4 여왕말 문제에 대해 되추적 알고리즘을 적용하는 과정</sub>
![](https://raw.githubusercontent.com/codingalzi/algopy/master/jupyter-book/imgs/algo05/algo05-06.png)
유망하지 않은 노드에서 가지치기를 하는 되추적하는 알고리즘은 그렇지 않은 일반 DFS보다 훨씬 적은 수의 노드를 탐색한다. 예를 들어 일반 DFS의 경우 155개의 노드를 탐색해야 하지만 되추적 알고리즘은 27개의 노드만 탐색한다
# n - 여왕말 문제
> 4 여왕말 문제를 일반화한 n - 여왕말 문제를 해결하는 되추적 알고리즘 구현

**문제의 변수, 도메인, 제약 조건**
- 변수: 1번무터 n번까지 이름이 붙은 n개의 여왕말
- 도메인: n\*n모양의 체스판에 포함된 1번부터 n번 열
- 제약 조건: 서로 다른 두개의 여왕말이 하나의 행, 열, 또는 대각선 상에 위치하지 않음
### 예제: 8 - 여왕말 문제
#### 상태 공간 트리
```python
from collections import defaultdict

# 변수: 네 개의 여왕말의 번호, 즉, 1, 2, ..., 8
variables = range(1, 9)

# 도메인: 각각의 여왕말이 자리잡을 수 있는 가능한 모든 열의 위치. 
# domains = 상태 공간 트리를 사전 형식으로 구현한 것
domains = defaultdict(list)

columns = range(1, 9)
for var in variables:
    domains[var] = columns
```
> [!summary]+ Output
> ```
> >> domains
> defaultdict(list,
>             {1: range(1, 9),
>              2: range(1, 9),
>              3: range(1, 9),
>              4: range(1, 9),
>              5: range(1, 9),
>              6: range(1, 9),
>              7: range(1, 9),
>              8: range(1, 9)})
> ```
#### 유망성 판단
배치된 여왕말의 정보를 저장하는 변수 `assignment`
```python
# 4개의 여왕발이 배치되었을 경우의 예시
assignment = # key : row, value : coluom
{
 1:1,
 2:5,
 3:8,
 4:6
}
```
배치된 말을 대상으로 다음 세가지 제약 조건이 성립함을 확인해야 한다
- 동일한 행에 위치하지 않기: 각각의 여왕말이 다른 행에 위치하도록 알고리즘이 작동하기에 자연스럽게 처리됨
- 동일한 열에 위치하지 않기: 서로 다른키에 대해 동일한 값이 사용되지 않도록 해야 함
- 동일한 대각선 상에 위치하지 않기: 두개의 여왕말 `q1`, `q2`가 동일한 대각선 상에 위치하려면 행과 열의 차이의 절댓값이 같아야 함
```python
abs(q1.r - q2.r) == abs(q1.c - q2.c)
```
아래 함수는 이미 배치된 여왕말을 대상으로 세개의 제약 조건이 만족하는지 여부를 확인함
```python
def promissing_queens(assignment=defaultdict(int)):

    # q1: 모든 여왕말 대상으로 유망성 확인
    for q1r, q1c in assignment.items(): # q1의 행과 열

        # q2 = 아랫쪽에 자리한 여왕말들과 함께 제약 조건 성립 여부 확인
        # q1r과 q2r은 자연스럽게 다름
        for q2r in range(q1r + 1, len(assignment) + 1): 
            q2c = assignment[q2r]
            if q1c == q2c:                       # 동일 열에 위치?
                return False
            if abs(q1r - q2r) == abs(q1c - q2c): # 동일 대각선상에 위치?
                return False 

    # 모든 변수에 대해 제약조건 만족됨
    return True 
```
#### 되추적 함수 구현
아래 `backtracking_search_queens()` 함수는 n-여왕말 문제를 되추적 기법으로 해결한다. 함수 정의에 사용된 변수들의 기능은 다음과 같다
- `num_queens`: 여왕말의 개수
- `variables`: 여왕말 번호
- `domains`: 각 여왕말의 도메인(영역). 여기서는 모두 1부터 `num_queens` 까지의 번호 사용.
- `assignment` 매개변수: 되추적 과정에서 이미 자리를 차지한 여왕말들의 위치 정보를 담은 사전 객체
- `unassigned`: 아직까지 자리를 잡지 못한 여왕말들의 번호로 구성된 리스트
- `first`: `unassigned` 에 포함된 여왕말 중에서 가장 낮은 번호의 여왕말. 즉, 이제 위치시켜야할 여왕말 번호.

함수 본체에 사용되는 `for` 반복문은 새로운 여왕말을 위치시키기 위해 모든 열을 대상으로 되추적 기법을 아래와 같이 적용한다.
- 유망성이 확인되면 되추적 기법을 재귀적으로 적용
- 유망성이 확인되지 않으면 바로 재귀 적용 중지 후 가장 가까운 조상 노드의 형제 노드로 이동하여 되추적 기법 재귀 적용
```python
def backtracking_search_queens(num_queens, assignment=defaultdict(int)):
    
    # 변수
    variables = range(1, num_queens+1)
    
    # 도메인: 각각의 여왕말이 위치할 수 있는 칸
    domains = defaultdict(list)

    columns = range(1, num_queens+1)
    for var in variables:
        domains[var] = columns
    
    # 재귀 종료 조건: 모든 변수에 대한 값이 지정된 경우
    if len(assignment) == len(variables):
        return assignment
    
    # 재귀 실행: 아직 자리 잡지 못한 여왕말이 존재하는 경우
    unassigned = [v for v in variables if v not in assignment]
    first = unassigned[0] # 다음 대상 여왕말
    
    # first 여왕말 위치시키기. 재귀 적용
    for value in domains[first]:
        # 기존의 assignment를 보호하기 위해 복사본을 활용함.
        # 되추적이 발생할 때 이전 할당값을 기억해 두기 위해서임.
        local_assignment = assignment.copy()
        local_assignment[first] = value

        # local_assignment 값이 유망하면 되추적 기법 재귀 적용
        # 즉, 다음 여왕말 대상으로 되추적 기법 적용
        if promissing_queens(local_assignment):
            result = backtracking_search_queens(num_queens, local_assignment)

            # 모든 여왕말을 위치시켰을 때 여왕말들의 정보 반환
            if result is not None:
                return result

    # 유망성 확인에 실패한 경우 재귀 종료. 즉 가지치기 실행.
    return None    
```
### n-여왕말 문제 되추적 알고리즘의 시간 복잡도
n 개의 여왕말이 주어졌을 때 상태 공간 트리에 포함된 노드의 수는 다음과 같다.
$$
1+n+n^2+n^3+⋯+n^n=\frac{n^n+1−1}{n−1}
$$
따라서 되추적 알고리즘이 탐색해야 하는 노드 수는 경우마다 다를 수 있지만 최대 n의 지수승 만큼 많은 수의 노드를 탐색해야 할 수도 있다. 하지만 이보다 더 효율적인 알고리즘은 아직 알려지지 않았다.