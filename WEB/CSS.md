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


