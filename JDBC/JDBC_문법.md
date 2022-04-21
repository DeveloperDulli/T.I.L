#### JDBC

* JDBC (Java Database Connectivity)
  
  * 자바에서 데이터베이스에 연결해 데이터를 주고 받을 수 있게 해주는 라이브러리
  
  * sql 명령문을 자바에서 수행하면 -> DB 전달 
  
  * DBMS의 종류에 따라서 JDBC 종류도 달라짐
  
  * Oracle -> JDBC
  
  * Connection 객체 생성 -> getConnection(url, username, userpw)
  
  * ex) try (Connection 이름 = DriverManager.getConnection(오라클의 접속유형 확인하여 일치하게 작성, username, userpw) ){
    
     }catch (Exceptoin e){
    
      e.printStackTrace();
    
    }

* PreparedStatement 
  
  * 객체를 생설할 때 인자값으로 넘겨주는 sql문(쿼리문)을 미리 DBMS에 컴파일하여 올려둠.
  - ex) String sql = "select * from 테이블명 where 컬럼명 = ?"
  
  - ?자리에 set되는 값을 말 그대로 값 그 자체로 들어가게 됨 (문자열 인식)
  
  - Statement 객체보다 preparedStatement 객체를 활요했을 때 가독성이 더 높아짐

* BasicDataSource
  
  * DBCP 를 만들어주는 클래스
  
  * ex) private BasicDataSource bds = new BasicDataSource();
  
  * ex) public 생성자이름(){ 
    
       bds.setUrl("jdbc:oracle:thin:ip주소:포트번호:xe");
       bds.setUsername("오라클계정명");
       bds.setPassword("계정비밀번호");
       bds.setInitialSize(커넥션 개수);
       }
