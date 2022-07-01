## JSP

* MVC (Model View Controller) : 디자인 패턴(코드를 짜는 방식)
  
  * Model : DB와 연동해 CRUD 작업을 하는 객체 -> DAO
  
  * View + Controller (현재)
    
    * main : Sysout(출력) / dao의 메서드를 호출(controller)
    
    * Servlet : controller / out.writer() -> 출력

* MVC2 패턴
  
  * Model : 기존과 동일하게 DB와 연동해 CRUD 작업하는 DAO
  
  * Controller : 기능 담당 + 클라이언트의 요청 / 응답처리
  
  * View : client에게 응답해줄 페이지를 꾸며주는 역할 -> jsp
    
    * 클라이언트의 모든 요청값이 controller를 거치게끔 만들어 줄 것

* EL(Expression Language) 
  
  * Servlet(controller)로부터 넘겨받은 request안에 있는 값을 꺼내서 사용하기 위해 필요한 언어

* ${key} : controller에서 setting 해줬던 key 값을 {} 안에 넘기면 그 key 값에 해당하는 값이 반환

* 배열/리스트 for문 돌리기 위해서 라이브러리 추가 필요
  
  * JSTL(Jsp / Java Tag Library)
  
  * -> script 영역이 아닌곳에서 for문 / if문을 사용할 수 있게 해줌
  
  * 라이브러리에 추가 후  사용하려는 jsp 파일 내에서 import 작업해주기
    
    -> <%@ taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %> 
  
  * <c:forEach items = "for문을 돌릴 리스트/배열" var = "리스트/배열 각 인데스에 담겨있는 배열">

* session
  
  * 클라이언트(웹 브라우저)가 서버에 접속하는 순간 (첫 요청값을 보내는 순간)
  
  * -> 서버가 지금 접속한 클라이언트에 대한 식별값을 하나 생성함(session id)
  
  * -> 서버는 식별 값을 이용해 HTTPSession 객체(저장소)를 생성

* SHA (Secure Hash Algorithm)
  
  * 안전한 해시 알고리즘
  
  * 다양한 길이를 가진 데이터를 고정된 길이값으로 변환하는 알고리즘
  
  * 복호화(암호화된 데이터를 원본데이터로 되돌릴 수 없음)가 불가능한 단방향 암호화 기법
  
  * SHA512 -> 원본데이터를 128byte의 무작위의 데이터로 변환

* Cookie
  
  * 클라이언트와 서버가 연결을 시도한 흔적을 남겼다가, 후에 또 연결을 시도할 시 과거의 접속을 이어나가기 위해 흔적을 사용하는 방법
  * ex) 로그인 시 아이디 기억하기 체크하고 로그인했을때 로그아웃 후 다시 페이지 들어갔을때 마지막에 입력된 아이디값이 자동으로 셋팅
