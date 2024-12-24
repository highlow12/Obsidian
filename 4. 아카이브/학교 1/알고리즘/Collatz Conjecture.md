---
tags:
  - programming/Algorythem/Recursion
aliases:
  - 콜라즈 추측
  - 우박수
  - 우박 수열
---
콜라츠 추측(Collatz Conjecture)은 양의 정수 $n$에 대해 다음과 같은 연산을 반복할 경우, 결국에는 항상 1에 도달한다는 추측입니다.
$$
f(n) = \begin{cases} n/2 & \text{if n is even}\\ 3n+1 & \text{if n is odd}\end{cases}
$$

이 추측은 아직 증명되지 않았으며, 모든 양의 정수에 대해 성립하는지는 알려져 있지 않습니다.  하지만 매우 큰 수를 포함하여 지금까지 테스트된 모든 수에 대해서는 1에 도달하는 것이 확인되었습니다.