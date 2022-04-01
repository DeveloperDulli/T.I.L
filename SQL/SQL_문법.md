### SQL 문법

- SELECT : 테이블에서 데이터를 조회
  
  - ex) SELCET * FROM 테이블명;
    
  - ex) SELECT 컬럼명 FROM 테이블명;
    
  - ex) SELECT 컬렴명 FROM 테이블명 WHERE 조건;
    

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

##### 조건문

- where
  
- order by : select 한 컬럼에 대해 정렬을 할 때 사용 하는 구문
  
  - ex) order by 컬럼명 ASC; 오름차순으로 정렬
    
  - ex) order by 컬럼명 DESC; 내림차순으로 정렬
    
  - 컬럼명 대신 인덱스 번호로 대체 가능
    

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

##### 숫자형 함수

* abs(숫자) : 인자로 전달받은 숫자의 절대값을 반환해주는 함수
* mod(숫자, 나눌 값) : 인자로 전달받은 숫자를 나눌 값으로 나눠서 나머지를 반환해주는 함수
* round(숫자, 소수점 인덱스 위치) : 인자로 받은 숫자를 지정한 위치 다음 자리수에서 반올림하여 반환해주는 함수

<img src = "https://github.com/DeveloperDulli/T.I.L/blob/master/SQL/img/sql_lower_upper_initcap.png">