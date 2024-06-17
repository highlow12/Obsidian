---
subject: DataStructure
tags:
  - Algorythem
---

- 해싱(hashing) : 키 값에 대한 산술적 연산에 의해 테이블의 주소를 계산하여 항목에 접근
- 해시 테이블(hash table): 키 값의 연산에 의해 직접 접근이 가능한 구조 
- 해시 함수(hash function)
	- 탐색키를 입력받아 해시 주소(hash address) 생성
	- 이 해시 주소가 배열로 구현된 해시 테이블(hash table)의 인덱스  
![[해시.png]]
# 해시 테이블
![[Hash Table]]
# 해시함수
![[Hash Function]]
# 해싱의 성능분석
- 적재 밀도(loading density) 또는 적재 비율(loading factor)
	- 저장되는 항목의 개수 n과 해시 테이블의 크기 M의 비율 
$$
\alpha =\frac{\text{저장된 항목의 개수}}{\text{해싱된 버켓의 개수}}= \frac{n}{M}
$$
- 선형 조사법에서의 비교 연산
$$
\text{실패한 탐색}=\frac{1}{2}\left(1 + \frac{1}{(1-a)^2}\right)
$$
$$
\text{성공한 탐색}=\frac{1}{2}\left(1 + \frac{1}{(1-a)}\right)
$$
- 체이닝에서의 비교 연산
$$
\text{실패한 탐색}=\alpha
$$
$$
\text{성공한 탐색}=1+\frac{\alpha}{2}
$$