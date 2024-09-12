# MVP (Model View Presenter)
>[!infobox] **모델-뷰-프리젠터**  
>![](https://upload.wikimedia.org/wikipedia/commons/thumb/d/dc/Model_View_Presenter_GUI_Design_Pattern.png/220px-Model_View_Presenter_GUI_Design_Pattern.png)
>##### Stats  
>- #DesignPattern
>- #ArchitecturePattern
>- #UI 

###### 모델
- 데이터와 데이터를 관리하는 규칙
- 모델은 뷰의 정보가 없다
###### 중재자 (Presenter)
- 모델과 뷰 사이에서 중재
- 뷰에서 입력 이벤트를 처리
- 게임의 조건이 변경되면 모델, 뷰를 업데이트
###### 뷰
- UI
- 사용자 상호작용을 중재자로 전송
- 뷰는 보델과 상호작용하지 않음
- 게임의 로직을 처리하지 않음
#### 로직
- 뷰는 입력을 중재자로 전송
- 중재자는 모델을 변경
- 모델으 ㅣ상태 변경 시 중재자에게 이벤트 통지
- 중재자는 수정된 데이터를 뷰로 전달 후 뷰는 UI 갱신
#### 장점
##### 확장성
- 특정 작업을 처리하는 부분들이 나뉘어 있으면 코드베이스 관리/확장이 용이
##### 모듈성
- 한 구성 요소가 전체 시스템에 영향을 끼치지 않음
- 각 구성 요소는 독립적으로 개발, 테스트, 수정 가능
- 디버깅 하기 용이
##### 재사용성 및 유지관리성
- 코드의 일부는 드른 부분에서 재사용 가능
- 스파게티 코드가 될 확률이 적음