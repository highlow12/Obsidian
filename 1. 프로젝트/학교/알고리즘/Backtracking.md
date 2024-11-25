---
tags:
  - programming/Algorythem
  - 수정중
aliases:
  - 백트래킹
  - 되추적 기법
---
# 되추적 기법
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
- [[State Space Tree]]
- [[State Space Tree#노드의 유망성|노드의 유망성]]
- [[State Space Tree#가지치기|가지치기]]
**DFS(깊이 우선 탐색)**
> 루트 트리를 대상으로 하는 모든 가능성을 탐색하는 일종의 완전 탐색<sub>brute force</sub>기법이다.

**과정**
- 루트 노드에서 시작하여 갈수 있는 한 가장 왼쪽 자식 노드로 탐색 진행
- 잎 노드에 도달한 경우 탐색 대상이 될수 있는 가장 가까운 노드로 이동해서 깊이 우선 탐색 진행, 단 한번 탐색한 자식 노드는 무시
위 과정을 실행하다가 더 이상 탐색 대상이 되는 노드가 존재하지 않을 경우 탐색 중지
> [!info]- DFS
>![[DFS]]

![[State Space Tree]]
![[n - Queen Problom#4 여왕말 문제 되추적 알고리즘]]
# 그래프 색칠하기