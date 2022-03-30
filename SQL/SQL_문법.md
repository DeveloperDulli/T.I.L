### SQL 문법



* SELECT : 테이블에서 데이터를 조회
  
  * ex) SELCET * FROM 테이블명;
  
  * ex) SELECT 컬럼명 FROM 테이블명;
  
  * ex) SELECT 컬렴명 FROM 테이블명 WHERE 조건;



##### 칼럼 산술 연산

* SELCET 컬럼명 * 숫자 FROM 테이블명;

* SELCET 컬럼명 as "별칭명" FROM 테이블명;
  
  * 컬럼 별칭 설정 -> as "별칭명" -> as 생략가능

* SELCET 컬럼명 || ' ****' FROM 테이블명;
  
  * 임의의 문자열을 실제 데이터 값처럼 보이게끔 리터럴 추가 가능 -> || 로 가능

* 연산자
  
  * = : 같다
  
  * < , > : 크다, 작다
  
  * != : 같지 않다
  
  * between A and B : 특정 범위에 포함되는지 (A이상 B이하)
  
  * like / not like : 문자 패턴 비교
  
  * is null / is not null : null 값 비교
  
  * in / not in : 특정한 값이 값 목록에 포함 여부
  
  

* like : 비교하려고 하는 값이 특정한 패턴을 만족시켰을 때 true 값을 반환하는 연산자
  
  * '%', '_' : 와일드카드(아무값이나 대체해서 사용할 수 있는 것)
  
  * % : 0글자이상 , _ : 한글자
  
  * 와일드카드 문자와 만약 문자열로써 사용하고픈 특수문자가 동일한 경우 -> 모두 다 와일드카드 문자로 인식

* escape 옵션
  
  * like '__ # __ ' escape '#' : #뒤로 오는 문자는 와일드 카드가 아닌 문자열로 인식



##### 조건문

* where 

* order by : select 한 컬럼에 대해 정렬을 할 때 사용 하는 구문
  
  * ex) order by 컬럼명 ASC; 오름차순으로 정렬
  
  * ex) order by 컬럼명 DESC; 내림차순으로 정렬
  
  * 컬럼명 대신 인덱스 번호로 대체 가능




