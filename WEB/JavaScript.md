### JavaScript

##### JavaScript

* 페이지에서 동적으로 요소를 다루고 변화시켜줄 수 있는 언어 (HTML로만 구성된 페이지는 정적인 페이지)

* 스크립트 언어
  
  * 한 줄씩 번역되면서 바로 실행이 되는 언어

* 컴파일 언어
  
  * 개발자가 짜놓은 코드를 기계어로 번역을 하고 실행

* 자바스크립트 사용방식
  
  * internal 방식 : body 태그 안쪽이나 혹은 head 태그 안쪽에 <script> 수행 코드</script>
  
  * external 방식 : 외부에 .js로 끝나는 스크립트 코드만 모아둔 파일을 아래와 같이 import해서 사용 
    
    * head영역에서 <script src = "js파일 경로"></script>
  
  * inline 방식 : 유지보수가 어렵기 때문에 잘 사용하지 않음
  
  * 요소 태그의 안쪽에 스크립트 코드를 추가하는 것도 가능

* 제어문
  
  * if, for 등 제어문을 활용해 다량의 요소도 컨트롤이 가능해짐
  
  * 다량의 요소를 찍어내거나, 특정한 상황에 따라서 동적인 변화를 주는게 다양해짐

##### 내장 함수

* alert : 브라우저에 기본적인 알림창을 띄워주는 함수, 인자값으로 넘긴 값이 랄림창 내용으로 들어감
  
  * alert("알림창");

* confirm : 확인과 취소 버튼 두 개를 띄워주는 알림창
  
  * 확인을 누르면 true 값을, 취소를 누르면 false 값을 리턴
  
  * 탈퇴, 게시글 삭제, 댓글 삭제 -> 한번 더 사용자에게 확인하는 용도로 사용
  
  * ex) confirm("알림창");

* prompt : 확인과 취소, 입력창을 띄워주는 알림창
  
  * 확인 누르면 입력값이 리턴 / 취소 누르면 null 값이 리턴
  
  * ex) promp("알림창");

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/WEB/JavaScript_img/alert.png">

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/WEB/JavaScript_img/confirm.png">

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/WEB/JavaScript_img/prompt.png">

##### 함수

* 함수의 생성 : 변환타입 x 매개변수의 자료형 x
  
  * function 함수(매개변수){
    
            // 처리할 코드
    
            // 만약에 리턴값이 있다면
    
            return 리턴값;}

* 자바스크리브의 함수는 마치 값처럼 사용하는게 가능

* 일급함수, first class function 라고도 함

* 익명 함수를 생성해서 변수에 담는 것도 가능

* 함수를 호출하면 호출한 자리 그대로 리턴값이 돌아옴

* 함수안에 함수를 생성하고 그 안에서 함수를 반환만 하는 것

##### 자료형

* 자바스크립트에서의 자료형
  
  * String, boolean, number, BigInt, null, Symbol, undefined
  
  * Symbol : 고유한 값을 만들고자 할 때 사용하는 자료형
  
  * undefined : 변수를 선언하고 그 변수에 값이 대입되지 않았을 경우 undefined가 default 값으로 잡힘
  
  * null : 값 자체가 없는 경우



##### 변수

* 자바스크립트에서는 변수에 명시적인 자료형이 붙지 않음

* 자바스크립트의 실행 흐름은 위에서 아래로 떨어짐

* var, let, const 로 모든 자료형을 담을 수 있음
  
  * var : function level scope / 변수를 선언하지 않은 상태에서 변수를 사용해도 에러가 나지 않음 / 중복된 이름의 변수 선언 가능
  
  * let : block level scope / 흔히 사용하는 변수
  
  * const : block level scope / 상수 (값 재할당 불가)
  
  * function level scope : 하나의 함수 내에서 선언한 변수는 해당 함수 내에서 공유되는 경우
  
  * block level scope : 하나의 블록 내에서 선언한 변수는 그 블록 내에서만 공유되는 경우 (자바에서의 지역(변수)과 비슷한 개념)

##### 요소 선택

* document 객체 : html 요소에 접근하는게 가능
  
  * 요소의 id 값을 이용해서 요소 선택
  
  * document.getElementById("요소의 ID");
  
  * -> 요소 그 자체를 가져옴
  
  * -> input, textarea, select 태그의 경우에는 그 안의 값을 가져올 때 value 속성을 이용해서 가져온다.
  
  * -> 다른 태그들은 innerHTML을 이용해 안에 있는 텍스트 값을 가져올 수 있음, html 요소를 추가하는 것도 가능, 스타일을 변경하는 것도 가능
