# Java 문법

1. 변수와 자료형 (Variable & Data Type)

변수 : 메모리에 하나의 값을 저장할 수 있는 방과 같은 기억 공간

기본 자료형

<img src="https://github.com/DeveloperDulli/T.I.L/blob/master/Java/img/Data%20Type.png">

2. 형변환 (Casting)
 
형변환(Casting) : 데이터의 자료형을 변환하는 것
* 개발자가 데이터의 타입의 범위를 예측하지 못했을 때

* 개발자가 원하는 대로 데이터 타입을 사용하기 위해서 강제적으로 형변환

* 자동 형변환 (promotion) : 작은 자료형에서 큰 자료형으로 변환이 이루어지는 경우

* 강제 형변환 (down casting) : 큰 자료형에서 작은 자료형으로 변환이 이루어지는 경우 (데이터의 손실이 일어날 수 있음)

3. 연산자 (Operator)

연산자 : 값 계산에 사용되는 계산용 기호 문자

기능에 따른 분류

<img src="https://github.com/DeveloperDulli/T.I.L/blob/master/Java/img/Operator.png">

삼항 연산자 : 조건식 ? 값1 : 값2  
* 조건식의 결과가 True일 경우 값1 반환, False일 경우 값2 반환, 조건식은 결과값이 반드시 boolean형 이다.

4. 제어문 (Control Statement)

* 조건문 : if - else문

<img src="https://github.com/DeveloperDulli/T.I.L/blob/master/Java/img/if%20-%20else.png">

* 반복문 (Loop문)
  * 문장들을 반복해서 여러 번 수행되게 할 때 사용하는 구문
    
  * 구문 상에 반복되는 구간을 루프(Loop)라고 하며, 루프가 있는 문장이라고 하여 루프(Loop)문이라고도 한다.

* for문
  * 가장 많이 사용되는 반복문으로 정확한 반복 횟수가 정해져 있을 때 주로 사용.
  * 배열이나 컬렌션의 연속 데이터 처리에 주로 사용

<img src="https://github.com/DeveloperDulli/T.I.L/blob/master/Java/img/for%EB%AC%B8.png">

* while문
  * for문과 다르게 반복에 대한 조건식만 제시되며 조건식의 결과가 true일 동안 수행영역 안의 내용이 반복적으로 실행되는 구조로 동작
  * 조건식의 결과가 false일 때 반복을 종료

<img src="https://github.com/DeveloperDulli/T.I.L/blob/master/Java/img/while.png">

* 중첩 반복문 : for문 안에 for문 또는 while문 안에 while문, for문 안에 while문, while문 안에 for문 등 반복문 종류에 상관없이 다양하게 중첩 가능
* break : 반복문의 실행 흐름에 변화를 줄 수 있는 문장으로, if문과 함께 사용되며 break문을 만나면 해당 반복문이 강제 종료
* conntinue : break문과 마찬가지로 반복문의 흐름에 변화를 주는 문장, 반복할 내용의 중간 생략용으로 이용할 수 있다.

5. 기본자료형 배열

* 배열 : 같은 자료형의 변수 여러개를 하나의 묶음으로 만들어 하나의 이름으로 다루는 것을 배열이라고 한다.
  * 자바에서는 배열 공간은 자유 메모리 영역인 Heap 영역에 할당하도록 지정되어 있으며, 배열변수는 할당된 배열공간의 주소를 저장하며, 배열공간의 주소를 이용해 인덱스(순번, index)를 참조하는 방식으로 값들을 처리하도록 정해두었다.

ex) 
<img src="https://github.com/DeveloperDulli/T.I.L/blob/master/Java/img/Array.png">