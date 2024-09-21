# MVC (Model View Controller)
>[!infobox] **모델-뷰-컨트롤러**  
>![](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a0/MVC-Process.svg/200px-MVC-Process.svg.png)
>##### Stats  
>- #programming/DesignPattern
>- #programming/ArchitecturePattern
>- #UI
>##### Important
> 각 레이어의 기능을 제한하여
> *[[SOLID 원칙#S 단일 책임 원칙|단일 책임 원칙]]*을 지치고자 한다



-  **모델**: 매플리케이션 데이터 관리
	- 값을 보간하는 데이터 컨테이너
	- 게임플레이 로직을 수행하거나 계산을 실행하지 **않음**
-  **뷰**: 데이터를 사용자에게 표시 (UI)
	- 화면에 데이터의 그래픽을 표현하는 인터페이스
-  **컨트롤러**: 입력 및 로직 처리
	- 데이터 처리, 런타임에 값이 어떻게 변하는지 계산
	- 입력을 처리하고 결과를 모델로 다시 전송
	- 그 자체로 게임 **데이터를 포함하지 않음**

MVC 적용 시 View는 문제가 없다.
그러나 모델 데이터의 변경 사항을 수싱하기 위한 뷰별 코드가 필요하다