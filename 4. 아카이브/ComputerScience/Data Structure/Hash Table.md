---
tags:
  - DataStructure
  - DataStructure/Table
subject: DataStructure
---
# 구조
- ![[해시테이블 구조.png|right|300]]
- **해시테이블**
	- M개의 버켓으로 구성된 테이블
	- 하나의 버켓에 S개의 슬롯이 가능하다 (충돌이 났을때 사용)
- **충돌(collision)**
	- 서로 다른 두개의 탐색키 k1, k2에 대하여 해시함수 h(k1) == h(k2)인 경우를 충돌이라고 한다
- **오버플로우(overflow)**
	- 충돌이 버킷에 할당된 값보다 많이 발생하는 것
	- 해결 방법이 반드시 필요하다

