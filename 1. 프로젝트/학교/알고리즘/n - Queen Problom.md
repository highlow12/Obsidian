---
tags:
  - programming/Algorythem
aliases:
  - 4 여왕말 문제
  - n 여왕말 문제
---

제약 충족 문제(CPS) 의 대표적인 예제
## 4 여왕말 문제
4 여왕말 문제는 1,2,3,4 네개의 여왕말이 4\*4 크기의 체스판에서 잡히지 않게 배치하는 문제
4 여왕말 문제를 정형화하면 다음과 같다
- 변수: 1부터 4까지 이름이 붙은 4개의 여왕말
- 도메인: 4\*4 모양의 체스판에 포함된 4개의 열
- 제약 조건: 서로 다른 두개의 여왕말이 하나의 행, 열, 대삭선 상에 존재하지 않음
![|200](https://raw.githubusercontent.com/codingalzi/algopy/master/jupyter-book/imgs/algo05/algo05-01a.png)
위는 앞서 언급된 제약 조건을 만족시키거나 아닌 경우를 보여준다
## n - 여왕말 문제