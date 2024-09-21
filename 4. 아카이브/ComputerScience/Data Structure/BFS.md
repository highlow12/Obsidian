---
tags:
  - Algorythem
  - Algorythem/Traversal
---
# 너비 우선 탐색
- 시작 정점으로부터 가까운 정점을 먼저 방문하고 멀리 떨어져 있는 정점을 나중에 방문하는 순회 방법
- 큐를 사용하여 구현됨
```
BFS(start):
    Create a queue Q
    Mark start as visited and enqueue start into Q
    while Q is not empty:
        v = Q.dequeue()
        for each neighbor u of v:
            If u has not been visited:
                Mark u as visited
                Enqueue u into Q

```
## 성능
- 인접 행렬: O(n^2)
- 인접 리스트: O(n+e)