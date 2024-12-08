---
tags:
  - programming/Algorythem
  - 수정중
  - programming/Algorythem/BruteForce
  - programming/Algorythem/DFS
aliases:
  - 백트래킹
  - 되추적 기법
---
## 주요 내용
- 제약 충족 문제
- 되추적 기법
- [[n - Queen Problom|n - 여왕말 문제]]
- 그래프 색칠하기
# 제약 충족 문제
> 제약 충족 문제constraint-satisfaction problem(CSP)는 여러 개의 대상 각각에 할당할 값을 특정 도메인(영역)에서 정해진 제약 조건에 따라 선택하는 문제이다.
## n - 여왕말 문제
![[n - Queen Problom]]

# 되추적 기법
## 관련 개념
- [[DFS]]
	- 루트 트리를 대상으로 하는 모든 가능성을 탐색하는 일종의 완전 탐색<sub>brute force</sub>기법이다.
- [[State Space Tree]]
- [[State Space Tree#노드의 유망성|노드의 유망성]]
- [[State Space Tree#가지치기|가지치기]]
### 과정
1. **[[DFS]] 탐색 실행**: 왼쪽 자식 노드로 이동
2. [[State Space Tree|노드의 유망성]] 판단
3. 노드의 유망성이 없다고 생각되면 [[State Space Tree#가지치기|가지치기]] 한다
위 과정을 실행하다가 더 이상 탐색 대상이 되는 노드가 존재하지 않을 경우 탐색 중지

## 활용 사례
- 스도쿠 퍼즐 해결
- 미로 찾기
- 최적 경로 탐색
- [[n - Queen Problom|n-여왕말 문제]]
- 그래프 색칠하기

## 장단점 비교
**장점**: 모든 가능성 탐색으로 정확한 해 도출 가능.

**단점**: 높은 시간 복잡도. 특정 문제에서는 비효율적.

## 관련 알고리즘
- [[동적 프로그래밍]]
- [[분기 한정법]]