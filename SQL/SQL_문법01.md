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

------------------------------------------------------------------------------------------------------------------------------

* Set Operator (집합 연산자)
  * 두 개 이상의 테이블을 조인 없이 연관된 데이터를 조회하는 방식
  * 여러 개의 질의 결과(ResultSet) 를 연결해서 하나로 결합하는 방식
  * 각 테이블에서 반환된 결과값을 하나의 테이블로 결합하는 방식
  * 여러 개의 sql 문을 사용해서 하나의 테이블로 결과를 반환받아야 하는 경우

** 조건 **

- select 절에서 조회하려는 컬럼의 수가 동일

- select 절의 동일 위치에 존재하는 컬럼의 데이터 타입이 상호 호환 가능

** 종류 **

* UNION / UNION ALL / INTERSECT / MINUS

###### UNION (합집합)

* 중복된 데이터를 제거하고 첫번째 컬럼을 기준으로 오름차순하여 데이터를 보여줌 

* 각 테이블에서 조회하는 컬럼 수가 다르면 UNION 사용 X

* 중복된 데이터는 출력이 안됨

    ex) select 컬럼명 from 테이블 A UNION select 컬럼명 from 테이블B;

###### UNION ALL (합집합)

* 중복된 데이터 제거하지 않고 정렬 없이 데이터를 그대로 보여줌

* 조회된 결과값의 첫번째 테이블 아래로 두번째 테이블 결과값을 그대로 이어붙이는 식

    ex) select 컬럼명 from 테이블A UNION ALL select 컬럼명 from 테이블B;

###### INTERSECT (교집합)

* 두 테이블의 쿼리 결과 중 공통된 결과 값만 보여줌

    ex) select 컬럼명 from 테이블A INTERSECT select 컬럼명 from 테이블B;

###### MINUS (차집합)

* 두 테이블의 쿼리 경과 중 공통된 요소를 뺀 한 테이블의 결과값만 보여줌
  
  ex) select 컬럼명 from 테이블A MINUS select 컬럼명 from 테이블B;

---

#### 서브쿼리 (SubQuery)

* 하나의 sql 문안에 포함된 다른 sql 문

* 메인 쿼리가 서브 쿼리를 포함하는 종속적인 관계

* 서브쿼리는 소괄호로 묶어주고 연산자의 오른쪽에 위치한다.

* order by 절은 서브쿼리 내에서 사용 불가능

###### 단일행 서브쿼리

* 서브커리 조회 결과 값이 1개(행)일 경우

* ex) select 컬럼명, 컬렴명 ... from 테이블명 where 조건 연산자 (select 컬럼명 from 테이블명);

###### 다중행 서브쿼리

* 서브쿼리 조회 결과가 여러개(여러 행)일 때.

* 다중행 서브쿼리 앞에는 = / ! = 연산자 사용불가

* in, not in, any, all, exists

* ex) select 컬럼명, 컬럼명 ... from 테이블명 컬럼명 다중행연산자 (select 컬럼명 from 테이블명 조건);

###### 다중열 서브쿼리

* 서브쿼리 조회결과 값이 여러개(열) 일 때

* 조건절의 컬럼명과 서브쿼리의 조회하는 컬럼명 동

* ex) select 컬럼명,컬럼명 ... from 테이블 where (컬럼명,컬럼명 ...) in (select 컬럼명, 컬럼명 ... from 테이블명 조건);



---

##### DDL (Data Definition Language)

* 데이터 정의어

* 데이터베이스 객체 생성 (CREATE), 수정 (ALTER), 삭제(DROP) 하는 구문

* 오라클 객체 종류 : 사용자 (user), 테이블 (table), 뷰 (view), 시퀀스 (sequence)...

* 테이블 생성 -> select table 테이블명 (컬럼명 자료형(크기), 컬럼명 자료형(크기).....);

* 테이블 수정 -> alter table 테이블명 추가/삭제/자료형 변경/ default 값 변경 (컬럼명 수정)

* 테이블 삭제 : drop table 테이블명;



###### 제약조건 (constraints)

* 테이블을 생성할 때 구성하는 컬럼에 들어갈 데이터에 대해 제약조건을 설정하는 것

* 데이터의 일관성과 정확성을 유지하기 위해서 (데이터 무결성)

* not null : 해당 컬럼에 null 값이 들어갈 수 없음

* unique : 중복된 값을 허용하지 않음

* primary key (기본) : null 값 허용 X, 중복값 허용 X -> 컬럼 중 고유 식별자

* foreign key (외래키) : 두 테이블 간의 관계를 설정하고 -> A테이블(id, pw, ....) B테이블(member_id, count ...) -> B테이블의 member_id 컬럼에 들어갈 수 있는 값이 A테이블의 id에 있는 데이터여야 하는 경우

* check : 해당 컬럼에 저장 가능한 값의 범위 조건을 지정해서 설정한 값만 허용



* 제약조건 거는 방식
  
  * create table 테이블명 (
    
    컬럼명 데이터타입 (크기) 제약조건,
    
    컬럼명 데이터타입 (크기) 제약조건,
    
    ....,);



###### 삭제 옵션

* 부모 테이블에서 데이터 삭제 할때 자식 테이블에 있는 데이터를 어떤 방식으로 처리할지 -> 제약조건을 걸 때 삭제 옵션도 걸어줌

* 기본 삭제 옵션은 on delete no action -> 자신을 참조하는 데이터가 있다면 삭제 할 수 없다.

* on delete set null -> 만약 참조하고 있던 부모 데이터가 삭제되면 자식 데이터를 null 값으로 설정

* on delete cascade -> 부모 데이터가 삭제되면 해당 데이터를 참조하고 있는 자식 데이터 역시도 함께 삭제
