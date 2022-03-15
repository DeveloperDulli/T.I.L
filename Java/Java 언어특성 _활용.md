# Java 언어특성 활용

* 객체지향프로그래밍 
  
  * 객체지향 프로그래밍이란 객체를 이용하는 프로그래밍 방식
  
  * 객체(Object)란 컴퓨터, 고객, 학생, 자동차 등 현실 시계에서 흔히 찾아볼 수 있는 대상을 추상화(Abstraction) 하여 프로그램 상에서 만들어낸 결과물



* 추상화(Abstraction) : 프로그램이 필요로 하는 실제 데이터들을 모델링하는 기술

* 캡슐화(EnCapsulation) : 객체 지향의 가장 중요한 데이터 보호 기술

* 상속(Inheritance) : 클래스의 재사용과 소스 코드의 중복 제거를 목적으로 하는 기술

* 다형성(Polymorphism) : 상속을 이용하여 여러 클래스 타입을 하나의 클래스 타입으로 다루는 기술



* 추상화와 캡슐화
  
  * 추상화 과정에서는 소스 코드의 구현이 아닌 데이터들의 객체화와 객체들 간의 관계에 대한 모델링 과정이 중요
  
  * 클래스(class)는 추상화한 내용을 정리한 설계도와 같은 것이고, 객체는 클래스를 실제 사용한 프로그램 상에서의 결과물

## 클래스(class)와 객체(Object == Instance)

* 클래스(class)    
  
  * 클래스는 객체를 만들기 위한 필요한 객체의 설계도
  
  * 자료형이 다른 변수들을 배열처럼 메모리에 연속 나열 할당하기 위한 순서를 지정하는 역할을 하며, 클래스 블록{}이 캡슐 즉 보호막의 역할을 하여 객체 외부에서 멤버변수(Field)로의 접근을 제한하며, 멤버변수들을 하나의 타입으로 묶어주는 것이 클래스
  
* 객체(Object)와 인스턴스(Instance)
  
  * 추상화가 이루어진 클래스로부터 데이터가 존재하는 실체로 만드는 과정을 인스턴스화라고 하며, 클래스로부터 만들어진 객체를 해당 클래스의 인스턴스라고 한다
  
  * 자바에서는 객체, 즉 인스턴스는 무조건 메모리 힙(Heap) 영역에 할당하도록 정하였으며 할당된 객체의 주소를 기록한 참조변수를 사용하여 객체를 참조하도록 정해두었다.

## 접근 제한자 (Access Modifier)

* public : 클래스 안과 밖, 패키지 안과 밖에 있는 모든 클래스들이 접근 가능
* protected : 비 상속시에는 default와 동일, 같은 패키지에 속한 클래스 간에만 멤버의 접근이 가능하며 다른 패키지에 있는 클래스일 때는 상속관계의 후손클래스 내에서만 부모클래스의 멤버에 접근이 가능
* default(package private) : 같은 패키지에 속한 클래스 간에만 멤버들에 대한 접근이 가능
* private : 멤버변수의 캡슐화를 위해 사용되는 제한자로 클래스 안에서만 접근이 가능하며 클래스 밖에서는 접근이 불가능

 * 접근 제한자의 공개 범위는 public>protected>default>private순으로 좁아지며, protected 접근제한자는 상속관계가 아니면 잘 사용하지 않는다.


###### private 필드 접근

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/Java/img/private.png">

###### public 필드 접근

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/Java/img/public.png">

###### protected 필드 접근

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/Java/img/protected.png">

###### default 필드 접근

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/Java/img/default.png">


## 클래스 구조

* 클래스는 헤더(Header) 시그니처(Signature)와 클래스 바디(Body)로 구성
* 클래스 헤더 시그니처는 클래스의 이름과 종류를 지정하는 부분이고, 클래스 바디 안에는 클래스의 멤버들이 정의되는 부분

###### 클래스 헤더

* [접근제한자][클래스식별자] class 클래스이름

* 접근제한자
 * public class 클래스명 : 패키지 안/밖 모두 접근(사용) 가능한 클래스
 * class 클래스명 : 선언된 패키지 안에서만 접근(사용) 가능한 클래스

* 클래스 식별자(identifier) : 클래스의 종류를 지정하는 예약어로 final, abstract 두 가지가 사용될 수 있다.
 * public final clasee : 종단 클래스, 더 이상 상속시킬 수 없는 클래스, 서브(후손) 클래스를 만들 수 없다.
 * public abstract class 클래스명 : 추상(미완성된)클래스, 상속을 이용해 후손 클래스가 부모의 미완성된 기능을 완성시킨다.