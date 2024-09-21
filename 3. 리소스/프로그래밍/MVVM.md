# MVVM (Model View Viewmodel)
>[!infobox] **모델-뷰-뷰모델**  
>![](https://upload.wikimedia.org/wikipedia/commons/thumb/8/87/MVVMPattern.png/500px-MVVMPattern.png)
>##### Stats  
>- #programming/DesignPattern
>- #programming/ArchitecturePattern
>- #UI 

###### 모델
- 데이터 구조
###### 뷰
- UI
- 뷰에 포함된 로직은 UI요소의 스타일 등에 관련
###### 뷰모델
- 뷰와 모델 사이의 중재자
- 뷰 상호작용시 모델을 업데이트 하는 역할
- 모델 변경시 뷰 업데이트 하는 역할
- 뷰모델과 뷰는 **데이터 바인딩**을 통해 연결

- 기존의 [[MVP]]에서 뷰와 컨트롤러/중재자의 의존성을 약화
- 마크업파일, 데이터 바인딩
- **데이터 바인딩**
	- 뷰와 뷰모델간의 데이터 바인딩으로 뷰모델 속성 변경이 **자동으로** 뷰에 반영
- 커맨드
	- 뷰모델에서 UI 상호작용을 처리하는 [[GoF#커맨드 (Command)|커맨드 패턴]] 사용
- 관심사 분리(SoC)
	- 뷰모델은 뷰에 대한 참조를 가지지 않으므로 테스트가 용이