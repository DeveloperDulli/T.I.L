## SQL

* 데이터 : 어떤 자료나 실제 값

* DB (DataBase) : 데이터가 저장되는 공간
  
  * 연관된 데이터를 최대한 중복없이 구조적으로 저장해 놓은 곳

* 특징
  
  * 실시간 접근성 : 사용자가 데이터를 요청하면 실시간으로 서비스
  
  * 계속적인 변화 : 최신 데이터를 유지
  
  * 동시 공유 : 서로 다른 업무를 하는 사용자들이 동시에 접속해서 데이터를 공유하는게 가능
  
  * 내용에 따른 참조 : 데이터의 물리적 주소값을 이용해 참조하는게 아니라 데이터가 가지고 있는 값에 따라 참조됨

* 장점
  
  * 테이블 단위로 저장
  
  * 테이블을 구성하는 데이터의 조건, 자료형 설정 
  
  * -> 사용자가 규정한 데이터만 저장되어 관리가능



* DBMS (DataBase Management System) : 데이터베이스에서 데이터를 추출, 조작, 정의, 제어 등을 할 수 있게 해주는 데이터베이스 전용 관리 시스템
  
  * 방대한 데이터는 있으나 관리자가 없으면 데이터를 수정, 삭제, 삽입, 조회 등이 불편함 -> 그래서 그런 역할을 DBMS가 해줌

* RDBMS (Realational DataBase Management System) : 행과 열로 구성된 Table 간의 관계를 나타내어 데이터를 표현하는 시스템 -> Oracle(oracle), Microsoft(MS-SQL), Oracle(MySQL), SQLite



* SQL (Structured Query Language) : 구조화된 질의 언어
  
  * 데이터베이스에서 데이터를 조회하거나 조작하기 위하여 사용하는 표준 언어
  
  * 사용하는 DBMS에 따라서 SQL 문법이 다름



* DML (Data Manipulation Language) 
  
  * 데이터 조작어, 데이터를 조작하기 위한 언어
  
  * 데이터의 INSERT(삽입), UPDATE(수정), DELETE(삭제), SELCET(조회) 등을 제어하는 언어

* DDL (Data Definition Language)
  
  * 데이터 정의어
  
  * 데이터베이스에서 개체(table, user...)를 정의하거나 변경, 삭제하기 위한 언어
  
  * DB관리자 설계자가 주로 사용
  
  * CREATE(생성), ALTER(수정), DROP(삭제), TRUNCATE(개체 초기화)

* DCL (Data Control Language)
  
  * 데이터 저어어
  
  * 사용자의 권한, 관리자 설정 처리하는 언어
  
  * GRANT(유저 권한 생성), REVOKE(유저 권한 삭제)
  
  

##### 오라클의 기본 데이터형

<img src = "">
