---
tags:
  - programming/Algorythem
  - programming/Algorythem/Search
  - programming/Algorythem/Divide_and_Conquer
---
# 이진 탐색
- 정렬된 배열의 중앙에 있는 값을 조사하여 찾고자 하는 항목이 왼쪽 또는 오른쪽 부분 배열에 있는지를 알아내어 탐색의 범위를 반으로 줄여가며 탐색 진행 
- (예) 10억 명중에서 특정한 이름 탐색
	- 이진탐색 : 단지 30번의 비교 필요
	- 순차 탐색 : 평균 5억 번의 비교 필요
- 시간 복잡도: [[빅-오 표기법|O(log n)]]
![[이진 탐색.png]]