---
tags:
  - Algorythem
  - Traversal
---

# 깊이 우선 탐색
- 한 방향으로 갈수 있을 때까지 가다가 더 이상 갈수 없게 되면 가장 가까운 갈림길로 되돌아가 다른 방향으로 다시 탐색 진행
- 되돌아가기 위해서 ==스택 필요==(순환함수 호출로 묵시적인 이용 가능)
## 재귀 호출을 사용한 방법
```
DFS(v):
    // v를 방문했음을 표시
    visited[v] = true
    // v와 인접한 모든 노드 u에 대해 반복
    for each u in adjacent[v]:
        if not visited[u]:
            DFS(u)
```
## 스택을 이용한 방법
```
DFS(start):
    스택 S를 생성하고, start를 S에 push한다.
    while S가 비어있지 않다면:
        v = S에서 pop한다.
        if v가 방문되지 않았다면:
            v를 방문 처리한다.
            v와 인접한 모든 노드 u에 대해:
                if u가 방문되지 않았다면:
                    S에 u를 push한다.

```
## 성능 분석
인접 행렬: O(n^2)
O()