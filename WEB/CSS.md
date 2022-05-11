### CSS

* css (Cascading Style Sheet)
  
  * 웹 페이지를 이루는 html 요소들의 스타일을 꾸며줄 수 있는 기능
  
  * -> html 요소들이 사용자들에게 어떤 시긍로 보일지를 결정해주는 기능

##### CSS 방식

* inline 방식 : html 요소의 태그 자체에 style 속성을 부여하는 방식

* 내부 스타일 시트 : 하나의 html 파일 안에서 <style> 태그를 이용해서 속성을 부여하는 방식

* external 방식 : 외부에 독자적인 stylesheet 파일을 만들어서 스타일 속성값을 별도로 모아두고, 그 파일을 import 해서 사용하는 방식

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/WEB/CSS_img/css.png">

* CSS 적용 우선순위 (중요도 / 명시도 / 선언순서)
  
  * 중요도
  
  * 1. 속성값 뒤에다가 !important
    
    2. inline 방식으로 적용된 style
    
    3. #id 선택자
    
    4. class, 가상 클래스 선택자
    
    5. tag 요소 선택자 (p, div, span)
  
  * 명시도 : 해당 요소를 명확하게 표현하게 할수록 우선순위 높아짐
  
  * 선언순서 : 하나의 요소에 대해서 여러개의 스타일 속성을 부여를 했을때 가장 마지막에 부여된 속성이 최우선순위를 지님

* 선택자 (Selector)
  
  * 전체 선택자(*) : 모든 html 태그를 선택
  
  * 태그 선택자 : 태그의 이름을 통해서 요소를 선택
  
  * id 선택자 (#) : 태그에다가 고유한 id 값을 부여해서 선택
  
  * class 선택자 (.) : 태그에 class 값을 부여해서 선

* Font 관련 style

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/WEB/CSS_img/font.png">

##### 속성 선택자

* 기본 속성 선택 : 태그자와 함께 사용하며, 태그 선택자[] {속성 표시}

* 문자열 속성 선택자 : 속성 값에서 특정한 문자열을 확인 스타일 적용
  
  * 태그 선택자[속성 ~= 값] : 속성 값이 특정한 값을 문자열로 포함하는 경우 선택(띄어쓰기 기준)
  
  * 태그 선택자[속성|= 값] : 속성 값이 특정한 값을 문자열로 포함하는 경우 선택(-기준)
  
  * 태그 선택[속성^=값] : 속성 값이 특정한 값으로 시작하는 태그를 선택
  
  * 태그 선택[속성$=값] : 속성 값이 특정한 값으로 끝나는 태그를 선택
  
  * 태그 선택[속성*=값] : 속성 값이 특정한 값을 포함하는 태그를 선택
  
  * not() 부정 선택자 : ()의 값이 아닌 경우 선택

##### 자식 / 후손 선택

* 자식 선택자 : 부모 요소를 기준으로 바로 아래 요소들
  
  * 부모 선택자 > 자식 선택자{설정 내용;}

* 후손 선택자: 부모 요소를 기준으로 아래의 모든 요소들
  
  * 부모선택자 자식선택자 {설정 내용;}

* 자식을 제외한 후손 선택
  
  * 부모선택자 * 후손선택자 {설정 내용;}

* 스타일 속성 중에서 몇몇 속성의 경우에는 상속이 적용돼서 부모에게 적용된 속성이 자식 요소한테도 모두 적용이 된다.

* 자식 요소를 기준으로 해서 사용하는 선택자
  
  * first-child : 첫번째 자식
  
  * last-child : 마지막 자식
  
  * nth-child() : ~번째 자식

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/WEB/CSS_img/selector.png">

##### 동위 선택자

* 동위 선택자 : 동위 관계에 있는 태그들을 선택할때 사용
  
  * 동위선택자a + 동위선택자b : a선택자를 통해 선택된 태그 바로 뒤에 있는 b선택자 태그만 선택
  
  * 동위선택자a~동위선택자b : a선택자를 기준으로 뒤에 오는 모든 b선택자에 해당하는 태그를 선택

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/WEB/CSS_img/selector02.png">

##### 반응 선택자

* 반응 선택자 : 사용자의 움직임에 따라서 달라지는 선택자
  
  * 선택자:active -> 사용자가 해당 태그에 마우스를 클릭했을때 선택이 됨.
  
  * 선택자:hover -> 마우스가 해당 요소 위에 올라가 있을 때 선택
  
  * 선택자:focus -> 해당 요소가 활성화된 상태이거나 클릭된 상태
  
  * 선택자:disabled -> 해당 요소가 비활성화된 상태라면
  
  * 선택자:checked -> 해당 요소가 체크되어있는 상태라면

##### 종속

* 일부 스타일 속성의 경우 무보의 속성이 자식의 속성에 영향을 미치는 '상속' 속성을 가짐
  
  * color, font, font-family, text-align 

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/WEB/CSS_img/inheritance.png">
