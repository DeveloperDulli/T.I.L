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
