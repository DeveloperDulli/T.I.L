### SQL 문법

###### 조인문 (JOIN)

* 두 개 이상의 테이블을 결합 하는 것
  
  * 조합하려고 하는 테이블에서 각 테이블의 공통된 컬럼을 데이터로 합쳐서 표현하는 것
  * 조건을 제시하지 않으면 Java의 이중 for문과 비슷한 형태로 동작 -> 모든 경우의 수를 조회
  * ANSI 표준 Join과 Oracle Join 으로 나눌 수 있음

* Cross Join (상호 조인)
  
  * 조인되는 테이블에 조건을 걸어주지 않아서 모든 데이터(모든 경우의 수가) 조합되어 나오는 경우
  * 한 테이블의 총 행수 * 다른 테이블의 총 행수
  * ex) select 컬럼명 from 테이블A, 테이블B;   -> Oracle Join
  * ex) select 컬럼명 from 테이블A cross join 테이블B;   -> ANSI Join

* Inner Join (내부 조인/교집합) 
  
  * 가장 많이 사용하는 Join 형태
  * 테이블A와 테이블B에서 조건이 맞는 데이터만 반환
  * ex) select 컬럼명 from 테이블A, 테이블B where 조건 ;   -> Oracle Join
  * ex) select 컬럼명 from 테이블A inner join 테이블B on (조건)/using(조건) ;   -> ANSI Join

* Outer Join
  
  * Left Outer Join (외부 조인/ 합집합 -> 왼쪽 외부 조인)
  * 조인하는 테이블A의 데이터를 모두 반환, 테이블B 조건 구문에만 일치하는 데이터만 반환
  * ex) select 컬럼명 from 테이블A, 테이블B where 컬럼 = 컬럼(+) ;   -> Oracle Join
  * ex) select 컬럼명 from 테이블A left outer join 테이블B on (조건)/using(조건) ;   -> ANSI Join
  * 
  * Right Outer Join (외부 조인/ 합집합 -> 오른쪽 외부 조인)
  * 조인하고자 하는 테이블A와 테이블B가 있을 때, 테이블 A는 조건 구문에 일치하는 데이터만 반환, 테이블 B는 조건에 상관없이 모든 데이터 반환
  * ex) select 컬럼명 from 테이블A, 테이블B where 컬럼(+) = 컬럼 ;   -> Oracle Join
  * ex) select 컬럼명 from 테이블A right outer join 테이블B on (조건)/using(조건) ;   -> ANSI Join

* Self Join 
  
  * 다른 테이블이 아닌 같은 테이블을 조인하는 것
  * 똑같은 테이블을 Join하기 때문에 각 테이블에 별칭을 반드시 지정하고 사용하려는 컬럼명을 어떤 별칭에 해당하는 컬럼명을 사용하려는건지 명확하게 해야함
  * ex) select 컬럼명 from 테이블A 별칭1 join 별칭2 on (별칭1.컬럼명 = 별칭2.컬럼명);

* Non_Equi Join (비등가 조인)
  
  * 지정한 컬럼의 값이 일치하는 경우가 아니라 값의 범위에 포함되는 행을 연결 (between, <, >, <= 등)
