1995년 GoF(Gang of Four)라고 불리는 Erich Gamma, Richard Helm, Ralph Johnson, John Vissides 가 처음으로 디자인 패턴을 구체화하였다. GoF의 디자인 패턴은 소프트웨어 공학에서 가장 많이 사용되는 디자인 패턴이다. 목적에 따라 분류할 시 생성 패턴 5개, 구조 패턴 7개, 행위 패턴 11개, 총 23개의 패턴으로 구성된다.

| ==범위==\\**목적** | **생성**                                                            | **구조**                                                                             | **행위**                                                                                                                                      |
| -------------- | ----------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| ==클래스==        | 1. Factory Method<br>                                             | 1. Adapter                                                                         | 1. Interpreter<br>2. Template Method                                                                                                        |
| ==객체==         | 1. Singleton<br>2. Abstract Factory<br>3. Builder<br>4. Prototype | 1. Bridge<br>2. Composite<br>3. Decorator<br>4. Facade<br>5. Flyweight<br>6. Proxy | 1. Chain of Responsibility<br>2. Command<br>3. Iterator<br>4. Mediator<br>5. Memento<br>6. Observer<br>7. State<br>8. Stratgy<br>9. Visitor |

# 생성 패턴
## 클래스
### 팩토리 메소드 (Factory Methd)
- 객체 생성을 서브클래스로 위임하여 캡슐화함
## 객체
### 싱글톤 (Singleton)
- 어떤 클래스의 인스턴스는 하나임을 보장하고 어디서든 참조할 수 있도록 함
### 추상 팩토리 (Abstrct Facory)
- 구체적인 클래스를 지정하지 않고 인터페이스를 통해 서로 연관되는 객체들을 그룹으로 표현함
### 빌더 (Builder)
- 복합 객체의 생성과 표현을 분리하여 동일한 생성 절차에서도 다른 표현 결과를 만들어낼 수 있음
### 프로토타입 (Prototype)
- 원본 객체를 복사함으로써 객체를 생성함
# 구조 패턴
## 클래스
### 어댑터 (Adapter)
- 
## 객체
### 브릿지 (Bridge)
### 컴포지트 (Composite)
# 행위 패턴
## 클래스
## 객체