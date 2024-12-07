---
tags:
  - DataStructure
  - DataStructure/Tree
  - DataStructure/Non-Linear
  - DataStructure/Array
---
**모든 이진 트리를 포화 이진 트리라고 가정하고 
각 노드에 번호를 붙여서 그 번호를 배열의 인덱스로 삼아 노드의 데이터를 배열에 저장하는 방법**
![[배열 이진 트리.png|600]]
## 부모와 지식 인덱스의 관계
- 노드 i의 부모 노드 인텍스 = i/2
- 노드 i의 왼쪽 자식 노드 인텍스 = 2i
- 노드 i의 오른쪽 자식 노드 인텍스 = 2i+1