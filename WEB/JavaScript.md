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

##### 자바스크립트 Object

* 속성의 집합
  
  * property(속성) = 자바에서의 멤버필드
  
  * key, value의 형태 = 자바에서는 멤버필드명이 key 멤버필드에 셋팅된 값이 value
  
  * ex) 이름 : tom  /  나이 : 20

* 객체 생성 / 사용법
  
  * 1. 객체 생성자
  
  <img src = "https://github.com/Hyung-Seok/T.I.L/blob/master/WEB/JavaScript_img/object.png">
  
  * 2. 생성자 함수
  
  <img title="" src="https://github.com/Hyung-Seok/T.I.L/blob/master/WEB/JavaScript_img/object02.png" alt="">
  
  * 3. 객체 리터럴
  
  <img src = "https://github.com/Hyung-Seok/T.I.L/blob/master/WEB/JavaScript_img/object02.png">
  
  * 생성자 내부에서 가능한 작업
    
    * ex) id라는 key에 해당하는 값 가져오기, ["키이름"]
  
  <img src ="https://github.com/Hyung-Seok/T.I.L/blob/master/WEB/JavaScript_img/object03.png">
  
  * 생성자 내부의 age 변수 값 가져오기
  
  * 생성자 내부에서 선언한 일반 변수는 private 속성을 가져서 외부에서 접근이 불가
  
  <img src = "https://github.com/Hyung-Seok/T.I.L/blob/master/WEB/JavaScript_img/object04.png">
  
  * 리터럴 방식으로 속성에 함수 값 넣기
  
  <img src = "https://github.com/Hyung-Seok/T.I.L/blob/master/WEB/JavaScript_img/object05.png">
  
  * 이미 만들어진 객체에 새로운 속성 추가

<img src = "https://github.com/Hyung-Seok/T.I.L/blob/master/WEB/JavaScript_img/object07.png">

##### 

##### 요소 선택

* document 객체 : html 요소에 접근하는게 가능
  
  * 요소의 id 값을 이용해서 요소 선택
  
  * document.getElementById("요소의 ID");
  
  * -> 요소 그 자체를 가져옴
  
  * -> input, textarea, select 태그의 경우에는 그 안의 값을 가져올 때 value 속성을 이용해서 가져온다.
  
  * -> 다른 태그들은 innerHTML을 이용해 안에 있는 텍스트 값을 가져올 수 있음, html 요소를 추가하는 것도 가능, 스타일을 변경하는 것도 가능

##### 배열

* 다양한 타입(자료형)의 데이터의 모음
  
  * 배열을 생성할때 자료형을 지정하지 않음
  
  * 문자열, 숫자, boolean, undefined, 객체, 함수

* 배열의 생성
  
  * ex) let arr = new Array(); , let arr = new Array(1,2,3);, let arr = [1, 2, 3];

* 배열의 값 넣기
  
  * index 번호 활용 (0번부터 인덱스 번호 시작)
  
  * let arr = ["봄", 30, false, function(){console.log("call function!")}, [1, 2, 3]]
  
  * -> 배열안에 여러 자료형 가능

* 배열 반복문
  
  * 자바의 foreach() 와 비슷하다 자바스크립트는 for..of
  
  * ex) for(let a of arr){console.log(e);} -> 처음부터 끝까지 출력

##### 배열 함수

* 배열 생성 -> 특정 값이 그 배열의 몇번 인덱스에 있는지 확인

* indexOf(값) : 값을 인자값으로 넘겨서 해당 배열의 가장 첫번째 값을 찾아 그 인덱스 반환 -> 만약에 인자로 넘겨준 값이 존재하지 않는다면 -1을 반환
  
  * ex) let tempArr = ['a', 'b', 'c', 'a'];
  
  * let index = tempArr.indexOf("a"); -> a가 0번째와 3번째에 있지만 0번을 출력

* concat(값/배열) : 값이나 배열을 결합해서 새로운 배열을 반환해주는 함수
  
  * 원본 배열에 영향을 주지 않음

* join(구분자) : 배열을 결합해 문자열로 반환
  
  * 하나의 배열안의 요소들을 모두 합쳐서 문자열로 반환
  
  * 인자값이 없을 경우 ,를 기준으로 요소들을 결합
  
  * 인자값으로 굽누자를 넘겨주면 해당 구분자를 기준으로 요소들을 결합
  
  * 원본배열은 영향받지 않음

* reverse() : 배열의 순서를 뒤집어주는 함수
  
  * 실제 원본 배열의 데이터 순서가 바뀜

* sort() : 배열안의 데이터를 오름차순 정렬 / 내림차순 정렬
  
  * 인자값 없이 사용했을 때는 문자열을 기준으로 오름차순 정렬

* push() : 배열의 가장 끝 인덱스에 새로운 값 추가

* pop() : 배열의 가장 끝 인덱스에 있는 값 삭제

* unshift(값) : 배열의 첫 인덱스에 새로운 값 추가
  
  * 원래 인덱스의 데이터들은 뒤 인덱스로 모두 밀려남

* shift() : 배열의 첫 인덱스 값 삭제

* slice(인자1, 인자2) : 배열을 잘라서 반환해주는 함수(배열에 값이 잘려진 상태를 반환)
  
  * 인자1 = 시작 인데스 -> 시작 인덱스에서부터 데이터를 잘라서 자른 데이터를 배열로 만들어 반환
  
  * 인자2 = 끝 인덱스 -> 시작 인덱스에서부터 데이터를 끝 인덱스까지 모두 잘라버림
  
  * 원본 배열 영향 없음
  
  * ex) let data = ["apple", "banana", "mango", "watermelon", "grape"];
  
  * -> data.slice(1, 3);  -> banana , mango

* splice(index, 제거수, [추가값]) -> 원본 배열에 영향을 줌
  
  * 시작 인덱스를 기준으로 해서 원하는 개수만큼 데이터를 제거할 수 있음
  
  * 세 번째 인자인 새로운 값을 추가하는 것도 가능한 함수
  
  * 시작 index : 해당 인덱스부터 값을 제거해라(만약 index 값만 인자로 넘겨주면 해당 인덱스부터 나머지 인덱스 데이터 모두 삭제)
  
  * 제거수 : 몇 개의 요소를 삭제할건지
  
  * ex) let data = ["apple", "banana", "mango", "watermelon", "grape"]; 
  
  * -> data.splice(2, 0, "melon") -> apple, banana, melon, mango, watermelon, grape

                

##### 코드의 실행 순서

* 위에서부터 아래로 실행

* window : 웹 브라우저의 모든 요소를 담는 객체

* window.onload : 웹 브라우저의 모든 요소들이 준비가 완료됐을때 function의 코드실행
  
  * ex) window.onload = function(){}

##### Event

- event : 브라우저 안에서 사용자가 취하는 모든 액션 (클릭, hover, drag, 스크롤, 크기조절 등등)

- call back function : 특정한 트리거(경우)가 있을때에만 호출되는 함수
  
  - 우리가 명시적으로 이벤트 관련 함수를 부른다고 호출이 되는게 아니라 특정한 이벤트가 일어났을때(클릭) 함수가 호출되는 것

- event listener(이벤트 감시자) : 특정한 이벤트가 발생했을 때 그 이벤트를 감지

- event handler(이벤트 처리자) : 특정한 이벤트가 감지됐을 때 그에 따른 처리코드를 수행하는 역할
  
  - 버튼을 눌렀을때 기능 수행 예시
  
  - ex) btn.onclick = function(e){수행 코드} -> btn버튼에 click 이벤트가 발생했을 때 특정한 코드를 수행
  
  - ex) btn.addEventListner("이벤트명", function() {처리코드} ) -> btn 버튼에 이벤트를 했을 때 특정한 코드를 수행

- mouseenter, mouseleave
  
  - mouseenter : 요소에 마우스가 올라갔을 때의 순간만 감지
    
    - ex) 아이디값.addEventListener("mouseenter", function(){처리 코드;});
  
  - mouseleave : 마우스가 요소 밖으로 떠났을 때의 순간만 감지
    
    - ex) 아이디값.addEventListener("mouseenter", function(){처리 코드;});

- 키보드 입력에 대한 이벤트 감지
  
  - keydown, keypress, keyup
  
  - keydown / keypress : 키보드를 입력하는 순간
  
  - keyup : 키보드 입력 후
  
  - ex) 아이디값.onkeyup = function(){처리코드;}; [다른것도 동일]
  
  - focus : input창에 커서가 깜빡이고 있는 상태
  
  - ex) 아이디값.onfocus = function(){처리 코드;}

##### 정규표현식

* 문자열에서 특정한 문자열을 추출해내고자 할 때 사용하는 표현

* 패턴 및 플래그
  
  * 패턴 : 대상이 되는 문자열을 찾는 패턴
  
  * 플래그 : 모든 문자 일치(g), 대소문자 구분 안함(i), 여러 줄 일치(m), 엔터키를 무시하고 모두 한 문장으로 인식(s-dotall)



* 메타 문자(패턴과 관련된 문자)
  
  * a | b : a 혹은 b 문자와 일치 (개수 상관 X)
  
  * [abc] : 괄호 안의 문자 중 하나와 일치 (개수 상관 X)
  
  * [^abc] : 괄호 안의 모든 문자 제외하고 일치 -> ^ 은 [] 안쪽에서만 부정의 의미로 쓰임
  
  * [a-z] : 괄호의 문자 범위 안의 모든 문자를 일치 
    
    * 대문자 영어 A-Z
    
    * 한글 ㄱ-힣
    
    * 숫자 0-9
  
  * \메타문자 : 이스케이프 문자 \와 함께 메타문자를 사용하면 문자열로써 인식이 가능



* 위치
  
  * ^a : 문장의 맨 앞에 있는 a 문자와 일치
    
    * multiline(다중행) 플래그를 걸어줘야 각 행의 시작값을 찾는 것이 가능
  
  * a$ : 하나의 행(문자)의 맨 끝의 문자와 일치시킴
  
  * ^abc$ : 정확히 abc인 값과 일치
  
  * a\b : 문자와 공백사이의 위치에 a가 있다면 일



* 수량자
  
  * a{n} : a가 정확히 n개인 경우 일치
  
  * a{n,} : a가 n개 이상 있는 경우 일치
  
  * a{n, m} : a가 최소 n개 이상 최대 m개 이하인 경우 일치
  
  * a* : a가 0개 이상인 경우 일치
  
  * a+ : a가 하나 이상인 경우 일치
  
  * a? : a가 0개 혹은 1개 있는 경우 일치

* greedy match (탐욕적 수량자)
  
  * a.*b : a라는 문자와 b라는 문자 사이에 어떤 문자가 오던간에 0개 이상있으면 일치 
    
    -> a와 b사이라는 조건이 안맞을때까지 모든 값을 일치 (여러개가 한문장에 있으면 다 포함)

* lazy match(게으른 수량자)
  
  * a.*?b : a와 b 사이의 조건이 일치하는 최소의 문자열만 일치



* 문자열 패턴
  
  * \d : 모든 숫자와 일치[0-9]
  
  * \D : 숫자 제외 모든 문자 일치
  
  * \s : 공백(띄어쓰기), 탭 문자와 일치
  
  * \S : 공백(띄어쓰기)과 탭 문자 제외한 모든 문자와 일치
  
  * \w : 한글 제외 모든 숫자, 영문자, 언더바와 일치
  
  * \W : 한글, 특수문자, 공백문자 등과 일치



* 그룹화
  
  * ( ) : 특정 문자열 패턴을 하나의 그룹으로 묶어서 관리할 수 있는 것
  
  * $& (캡쳐변수) : 정규식을 통해 선택된 데이터가 자동으로 저장되는 변수
  
  * $1 : 1번 그룹의 데이터를 담고 있는 변수



* singleline flag : 여러 문장을 하나의 문장으로 만들어 엔터키를 무효화 시킴.



* 정규표현식을 사용하기 위해 표현식 생성법
  
  * /패턴/ -> 슬래시를 사용하면 표현식이 생성된다.
  
  * ex) let regex = /패턴/;
  
  * RegExp 생성자 사용
  
  * let regex = new RegExp(/패턴/);

* RegExp 함수
  
  * test(대상 문자열) : 대상 문자열을 기준으로 패턴식에 일치하는 문자열이 있으면 true / false 를 반환
  
  * exec(대상 문자열) : 대상 문자열을 기준으로 패턴식에 일치하는 문자열을 찾아 배열로 반환, 못찾으면 null 반환
  
  * 표현식.test(대상 문자열) : 포인터가 있어 한 번 실행이 되고 나면 결과값을 기억하는데 g 플래그를 붙여주지 않으면 포인터가 초기화 됨
  
  * 표현식.exex(대상 문자열) : 대상 문자열이 있으면 배열 / null, g옵션 안주면 포인터 초기화
    
    * 0번 : 일치하는 문자열
    
    * index : 일치하는 문자열의 인덱스
    
    * input : 대상 문자
  
  * 대상문자열.search(표현식) : 가장 처음 일치하는 문자열의 인덱스 값이 반환, 일치하는 문자열이 없을 때에는 -1 반환 -> 여러번 사용해도 첫번째 일치하는 문자열을 기준
  
  * 대상문자열.match(표현식) : 일치하는 문자열의 배열을 반환해주는 함수 -> 일치하는 값이 없으면 null 반환
  
  * 문자열.replace(대상 값, 변환할 값) : 문자열에서 대상 값을 변환할 값으로 변환
  
  * 문자열.replace(표현식, 변환할 값)

* String 함수
  
  * 대상 문자열.match(패턴식) : 대상 문자열을 기준으로 패턴식에 일치하는 문자열이 있다면 배열로 반환
  
  * 대상 문자열.search(패턴식) : 대상 문자열 기준으로 패턴식에 일치하는 문자열의 인덱스를 반환, 못찾으면 -1 반환

* 표현식 반복문
  
  * 표현식을 for문 안쪽에서 선언하면 반복문이 돌때마다 표현식이 초기화되면서 함수가 첫 번째 값을 기준으로만 동작

##### 유효성 검사

* 클라이언트쪽에서 사용자의 입력값에 대해서 유효한 값인지 검사하고 유효하지 않다면 서버에 애초에 전송되지 않도록 알림을 띄워주거나 style을 이용해 경고문구 띄워줌. 중간에 코드의 흐름을 막아주기 위해서는 return 키워드를 활용

* 정규식
  
  * 아이디값을 6~10자 이내로 영어, 숫자 조합으로 만드시오.
  
  * ex)  /^[a-zA-Z0-9]{6,10}$/
  
  * 비밀번호를 6~15자 이내로 영어, 숫자, 특수문자(!@#%)를 포함하시오.
  
  * ex)  /^[a-zA-Z0-9!@#%]{6, 15}$/
  
  * 이메일을 영어,숫자 @ 영어.(com, net, co, kr, or, kr)로 표현하시오.
  
  * ex) /^[a-zA-Z][\w]+@[a-zA-Z]+\.(com|net|co\.kr|or\.kr)$/
