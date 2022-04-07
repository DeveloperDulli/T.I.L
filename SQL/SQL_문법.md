### SQL 문법

- SELECT : 테이블에서 데이터를 조회
  
  - ex) SELCET * FROM 테이블명;
    
  - ex) SELECT 컬럼명 FROM 테이블명;
    
  - ex) SELECT 컬렴명 FROM 테이블명 WHERE 조건;
    
------------------------------------------------------------------------------------------------------------------------------

##### 칼럼 산술 연산

- SELCET 컬럼명 * 숫자 FROM 테이블명;
  
- SELCET 컬럼명 as "별칭명" FROM 테이블명;
  
  - 컬럼 별칭 설정 -> as "별칭명" -> as 생략가능
- SELCET 컬럼명 || ' ****' FROM 테이블명;
  
  - 임의의 문자열을 실제 데이터 값처럼 보이게끔 리터럴 추가 가능 -> || 로 가능
- 연산자
  
  - = : 같다
    
  - < , > : 크다, 작다
    
  - != : 같지 않다
    
  - between A and B : 특정 범위에 포함되는지 (A이상 B이하)
    
  - like / not like : 문자 패턴 비교
    
  - is null / is not null : null 값 비교
    
  - in / not in : 특정한 값이 값 목록에 포함 여부
    

- like : 비교하려고 하는 값이 특정한 패턴을 만족시켰을 때 true 값을 반환하는 연산자
  
  - '%', '_' : 와일드카드(아무값이나 대체해서 사용할 수 있는 것)
    
  - % : 0글자이상 , _ : 한글자
    
  - 와일드카드 문자와 만약 문자열로써 사용하고픈 특수문자가 동일한 경우 -> 모두 다 와일드카드 문자로 인식
    
- escape 옵션
  
  - like '__ # __ ' escape '#' : #뒤로 오는 문자는 와일드 카드가 아닌 문자열로 인식

------------------------------------------------------------------------------------------------------------------------------

##### 조건문

- where
  
- order by : select 한 컬럼에 대해 정렬을 할 때 사용 하는 구문
  
  - ex) order by 컬럼명 ASC; 오름차순으로 정렬
    
  - ex) order by 컬럼명 DESC; 내림차순으로 정렬
    
  - 컬럼명 대신 인덱스 번호로 대체 가능
    
------------------------------------------------------------------------------------------------------------------------------

##### 문자형 함수

* dual 테이블 : 오라클에서 제공해주는 연산, 함수 실행 용도로 사용하는 특수한 테이블*    
* instr (컬럼/문자열, 찾고자 하는 문자(열), 시작 인덱스, 검색된 문자(열)의 순번) : 특정 문자열에서 찾고자 하는 문자열을 찾아주는 함수

ex)

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/SQL/img/sql_instr.png">

* lpad /rpad(대상이 되는 컬럼/문자열, 반환할 길이, 덧붙일 문자)
  
  * 주어진 컬럼/문자열을 대상으로 해서 임의의 문자열을 왼쪽/오른쪽에 덧붙여서 길이 N의 문자열을 반환하는 함

ex)   

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/SQL/img/sql_rpad.png"> 

* ltrim/rtrim (대상이 되는 컬럼/ 문자열, 제거하고 싶은 문자(열))
  
  * 주어진 컬럼/문자열을 대상으로 제거하고 싶은 문자를 제거한 뒤 나머지를 반환하는 함

ex)    

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/SQL/img/sql_ltrim.png">

* substr (대상이 되는 컬럼/문자열, 문자열을 잘라낼 위치, 반환할 문자의 개수)
  
  * 대상이 되는 컬럼/문자열에서 시작위치로부터 제시한 문자의 개수만큼 문자(열)을 잘라서 반환해주는 함수

ex)

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/SQL/img/sql_substr.png">

* concat (대상문자열1, 대상문자열2) 
  * 두개의 문자열을 하나로 합친 후 반환해주는 함수

ex)

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/SQL/img/sql_concat.png">

* lower(대상 문자열/컬럼) / upper(대상 문자열/컬럼) / initcap(대상 문자열/컬럼)
  * lower : 대상 문자열을 모두 소문자로 변환해주는 함수
  * upper : 대상 문자열을 모두 대문자로 변환해주는 함수
  * initcap : 단어의 첫 글자만 대문자로 변환해주는 함수

ex)

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/SQL/img/sql_lower_upper_initcap.png">

* replace(대상이 되는 문자열/컬럼, 변경대상이 되는 문자(열), 변경할 문자(열))
  * 대상이 되는 문자열/컬럼을 기준으로 변경대상이 되는 문자(열)을 찾아서 변경할 문자(열)로 바꿔주는 함수

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/SQL/img/sql_replace.png">

------------------------------------------------------------------------------------------------------------------------------

##### 숫자형 함수

* abs(숫자) : 인자로 전달받은 숫자의 절대값을 반환해주는 함수
* mod(숫자, 나눌 값) : 인자로 전달받은 숫자를 나눌 값으로 나눠서 나머지를 반환해주는 함수
* round(숫자, 소수점 인덱스 위치) : 인자로 받은 숫자를 지정한 위치 다음 자리수에서 반올림하여 반환해주는 함수

ex)

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/SQL/img/sql_lower_upper_initcap.png">

* floor (숫자, 소수점 인덱스 위치) :  인자로 받은 숫자를 지정한 위치 다음 자리수에서 반올림하여 반환해주는 함수
* trunc (숫자, 소수점 위치) : 인자로 받은 숫자를 지정한 위치까지 잘라서 반환해주는 함수
* ceil (숫자) : 인자로 받은 숫자의 소수점 자리를 올림한 후 버리고 반환해주는 함수

ex)

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/SQL/img/sql_floor_trunc_ceil.png">

------------------------------------------------------------------------------------------------------------------------------

##### 날씨 함수

* sysdate : 시스템에 저장되어있는 현재 날짜 (시간포함) 반환
* current_date : session(접속) timezone에 따라 현재 날짜(시간) 반환
  * ex) select sysdate from dual;
  * ex) select current_date from dual;

* months_between (날짜형, 날짜형) : 두 날짜 사이의 개월 수 차이를 반환해주는 함수
* add_months (기준 날짜, 더할 개월 수) : 첫 번째 인자값인 날짜를 기준으로 해서 두 번째 인자값을 더해서 반환해주는 함수
  * ex) select add_months(sysdate, 1) from dual; -> 현재 날짜보다 1개월 더한값
  * ex) select add_months(sysdate, -1) from dual; -> 현재 날짜보다 1개월 뺀값

* next_day (기준 날짜, 요일/숫자) : 기준 날짜를 기준으로 해서 오른족에 해당하는 가장 가까운 날짜를 반환해주는 함수
  * 요일의 형식 : '월' 혹은 '월요일'
  * 숫자의 의미 : 1 = 일요일 ~~ 7 = 토요일

* last_day (기준 날짜) : 기준 날짜의 바탕으로 해서 해당 날짜가 속한 달의 마지막 날을 반환해주는 함수
* extract (year/month/day from date(기준날짜)) : 기준날짜로부터 년/월/일을 추출해서 반환해주는 함수
  * ex) select extract (year from sysdate) from dual; : 현재날짜의 '년도' 반환
  * ex) select extract (month from sysdate) from dual; : 현재날짜의 '월' 반환
  * ex) select extract (day from sysdate) from dual; : 현재날짜의 '일수' 반환

------------------------------------------------------------------------------------------------------------------------------

##### 형 변환

* to_char (date/number, formate) : 날짜 혹은 숫자를 특정한 형식의 문자형으로 변환해주는 함수
  * 년 : YY / YYYY
  * 월 : MM
  * 일 : DD
  * ex ) select to_char(sysdate, 'YYYY-MM-DD') from dual; -- YYYY-MM-DD
  * ex ) select to_char(sysdate, 'YYYY/MM/DD') from dual; -- YYYY/MM/DD

* DAY : x요일
  * ex) select to_char(sysdate, 'YY/MM/DD/DAY') from dual; --  YY/MM/DD/x요일
* DY : x(요일)
  * ex) select to_char(sysdate, 'YY/MM/DD/DY') from dual; --  YY/MM/DD/x
* MONTH : x월
  * ex) select to_char(sysdate, 'YY/MONTH/DD') from dual; --  YY/MM월/DD
* HH MI SS : 시분초
  * ex) select to_char(sysdate, 'HH:MI:SS') from dual; --  HH:MI:SS
* PM/AM : 오후/오전
  * ex) select to_char(sysdate, 'PMHH:MI:SS') from dual; --  오후HH:MI:SS
* HH24 : 24시간을 기준으로 표기
  * ex) select to_char(sysdate, 'HH24:MI:SS') from dual; --  HH:MI:SS (24시간 기준으로 표기되기 때문에 오후1시면 13시로 표기됨)

* to_char (대상 숫자,  )
  * 숫자 -> 문자형
  * 123456789 -> 0이나 9를 이용해 문자형으로 변환
  * 9 : 지정해준 형식보다 짧은 숫자가 들어온다면 대상이 되는 숫자 길이에 맞춰서 결과값을 반환
  * 0 : 지정해준 형식보다 짧은 숫자가 들어온다면 형식에 맞춰서 길이를 지정하고 남는 자리수는 0으로 채워줌

ex)

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/SQL/img/sql_to_char.png">

* to_date (숫자/문자, 형식) : 숫자형 혹은 문자형 데이트를 데이트(날짜) 타입으로 바꿔주는 함수

ex)

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/SQL/img/sql_to_date.png">

* to_number (문자형, 형식) : 문자형을 숫자형으로 반환해주는 함수

ex)

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/SQL/img/sql_to_number.png">

* 통화 표시 : L (local)
  * ex) select to_char(12345,'L999,999') from dual; -- ￦12,345

* 묵시적 형변환
  * 오라클에서는 어느 정도 자동적으로 자료형을 유추해서 형변환
  * 하지만 묵시적 형변환에 의지하면 안되고 정확한 연산을 위해서는 정확한 자료형으로 변환한 후에 연산

------------------------------------------------------------------------------------------------------------------------------

##### 그룹함수

* sum (숫자/컬럼) : 해당 컬럼/숫자 값의 총 합을 구해주는 함수
  * ex) select sum(숫자/컬럼) from 테이블명;

* avg (컬럼) : 해당 컬럼 값들의 평균을 구해주는 함수
  * ex) select avg(컬럼) from 테이블명;

* count (컬럼) : 해당 컬럼 -> 데이터의 개수를 반환해주는 함수
  * select count(컬럼) from 테이블명

* max/min (컬럼) : 해당 그룹에서 최대값/최소값을 반환해주는 함수
  * ex) select max(컬럼) from 테이블명;	  -- 최대값
  * ex) select min(컬럼) from 테이블명;   -- 최소값

* group by : 그룹함수를 이용해 여러 개의 결과값을 도출하고 싶을 때
  * 그룹함수는 단 한개의 결과값에 도출
  * 그룹함수가 적용될 그룹 기준으로 해서 group by 절에 해당 그룹을 (컬럼) 기술해 사용
  * 함수를 적용한 컬럼도 사용 가능
  * 해당 절에 여러 컬럼값을 넘기는 것도 가능 ->왼쪽부터 그룹화가 순차적으로 진행
  * ex) select 그룹함수(컬럼) from 테이블명 group by 컬럼명;

* having : group by를 이용해서 그룹함수로 값을 구해올 때 그 값에 대한 조건을 걸고 싶다면 사용하는 절
  * ex) select 그룹함수(컬럼) from 테이블명 group by 컬럼명 having 조건;

------------------------------------------------------------------------------------------------------------------------------

조건식

* decode 조건문
* decode (대상표현식, 조건1, 결과1, 조건2, 결과2, default)
  * 대상표현식/값이 조건1과 같다면 결과1이 반환, 조건2와 같다면 결과2가 반환, 이 모든 조건이 충족되지 않는다면 default 값이 반환
  * 만약 default 값을 명시적으로 지정해주지 않으면 default = null
  * equal 비교만 가능
  * ex) select decode(substr(123456,1,1), '1', '하나', '2', '둘', null) from dual; -- 하나 출력

* case 조건문

select

    case

        when 조건1 then 결과1

        when 조건2 then 결과2

        ....

        else

    end

from dual;

-> 조건1이면 결과1 출력

-> else 모든 조건이 충족되지 않으면 반환되는 결과

-> else (기본값)을 설정해주지 않으면 조건이 모두 맞지 않을때 null 값 반환

-> case를 이용해서 결과값을 적어줄 때 모든 조건에 대해 동일한 자료형 사용



