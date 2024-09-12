---
tags:
  - programming
  - DesignPattern
  - ArchitecturePattern
  - UI
---
> [!important]+ 
> - UI와 로직의 분리가 목적
> - 불필요한 종속 관계를 줄임
> - 잠재적으로 스파게티 코드 방지
> - UI/UX 프레임워크에 의존적

# MVC (Model View Controller)
>[!infobox] **모델-뷰-컨트롤러**  
>![](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a0/MVC-Process.svg/200px-MVC-Process.svg.png)
>##### Stats  
>- #DesignPattern
>- #ArchitecturePattern
>- #UI



-  **모델**: 매플리케이션 데이터 관리
	- 값을 보간하는 데이터 컨테이너
	- 게임플레이 로직을 수행하거나 계산을 실행하지 **않음**
-  **뷰**: 데이터를 사용자에게 표시 (UI)
	- 화면에 데이터의 그래픽을 표현하는 인터페이스
-  **컨트롤러**: 입력 및 로직 처리
	- 데이터 처리, 런타임에 값이 어떻게 변하는지 계산
	- 입력을 처리하고 결과를 모델로 다시 전송
	- 그 자체로 게임 **데이터를 포함하지 않음**
# MVP (Model View Pre)