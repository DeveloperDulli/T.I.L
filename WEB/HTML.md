#### HTML

* HTML (Hyper Text Markup Language)
  
  * 웹 페이지를 구성하는 언어
  
  * Markup Language : 구조화된 언어 -> 각각의 요소들을 태그로 구조화 시킨 언어
  
  * -> A라는 태그를 보면 이런 의미를 가지고 있구나 해석할 수 있게끔 함

* HTTP(HyperText Transfer Protocol)
  
  * 웹에서 이뤄지는 모든 데이터 교환(클라이언트-서버)은 HTTP 통신규약을 통해 이루어진다.

* Structure

    <img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/WEB/HTML_img/structure.png">

* 하이퍼링크

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/WEB/HTML_img/tag.png">

##### 강조 관련 태그

* h1 ~ h6
  
  * 제목을 표시하기 위해 사용하는 태그
  
  * 숫자가 작을수록 가장 중요한 제목, 클수록 덜 중요한 제

* em
  
  * 강조하는 택스트에 사용
  
  * 기본 모양을 기울림꼴

* strong
  
  * 중요한 텍스트에 사용
  
  * 기본 모양은 굵은 글자

* b
  
  * 글자를 굵게 만듬
  
  * 의미 없이 굵게 만드는 것이 strong과의 차

* underline
  
  * 글자 아래에 밑줄을 만

##### 문단

* display 속성 : block 속성(16px margin) / inline 속성
  
  * block 속성 : 요소의 전후 줄바꿈을 한 후에 무조건 한 줄을 차지하는 속성
  
  * ex) p 태그, div 태그 등등
  
  * inline 속성 : 해당 태그가 가지고 있는 컨텐츠의 크기만큼만 자리를 차지
  
  * ex) span 태그 등등

##### list

* ul 태그 : 순서가 없는 리스트

* ol 태그 : 순서가 있는 리스트

* type 속성 : 숫자, 아라비아 숫자, 알파벳 순서를 매길지 결정해줄 수 이씀

* start : 시작점 지정 가능

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/WEB/HTML_img/list.png">

##### Input 태그

* input 태그 : 사용자의 입력값을 받기 위해 사용하는 요소

* placeholder : 어떤 값을 입력할지 안내해주는 역할

* value : input 창에 실제로 입력되는 데이터

* readonly : input 창에 있는 고정 값 (읽기 전용 창)

* maxlength : input 창에 입력값 길이 고정

* password : 사용자의 입력값을 받을 때 값을 보호함

* email : 입력받은 값이 유효한 이메일 주소인지를 자동으로 검증하는 입력 필드 생성
  
  <img title="" src="https://github.com/DeveloperDulli/T.I.L/blob/master/WEB/HTML_img/input01.png" alt="">

* checked : checked 속성을 준 태그에 기본으로 항목 선택함

* radio : 여러개의 값 중 하나만 체크하고 싶을때 사용

* checkbox : 여러개의 선택지에서 여러개의 선택값을 받고 싶을때 사용

* select : 여러개의 옵션값을 미리 깔아두고 사용자가 선택하게끔 하는 입력방식

* date : 날짜를 입력할때 사용

* color : 색상을 입력할때 사용

* range : 범위를 조절할때 사용

* button : 버튼을 생성할때 사용

* text : 일반적으로 한 줄짜리 입력을 받을때 사용

* textarea : 여러 줄의 텍스트 입력값을 받을 때 사용 (width : 넓이, height : 높이, 
  
  resize : 사이즈 조절)

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/WEB/HTML_img/input02.png">

##### table 구성

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/WEB/HTML_img/table.png">
