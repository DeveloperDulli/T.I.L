## Amazon Web Services

-------------------

#### AWS(Amazon Web Services)

* 아마존의 클라우드 플랫폼

* 아마존 웹 서비스는 다른 웹 사이트나 클라이언트측 응용 프로그램에 대해 온라인 서비스를 제공하고 있음

* 이러한 서비스의 상당수는 최종 사용자에 직접 공개되는 것이 아니고, 다른 개발자가 사용 가능한 기능을 제공하는 플랫폼을 제공하는 PaaS이다.
  
  * Paas : Platform as a Service 서비스로서의 플랫폼
  
  * 클라우드 컴퓨팅 서비스 분류 중 하나
  
  * SaaS의 개념을 개발 플랫폼에도 확장한 방식으로, 개발을 위한 플랫폼을 구축할 필요 없이 필요한 개발 요소를 웹에서 쉽게 빌려쓸 수 있음
  
  * 구글의 앱 엔진 같은 public API의 경우 직접 온라인 서비스를 개발에서 배포, 관리까지 할 수 있는 플랫폼을 제공하고 있음
  
  * Saas : Softare as a Service 서비스로서의 소프트웨어
  
  * 주문형 소프트웨어라고도 부르며, 고객 관리 영역이나 회계쪽 분야에서 사용

#### EC2 (Elastic Compute Cloud)

* Aws에서 가장 중요한 서비스

* 아마존이 서비스를 제공하는 리전에서 가상의 컴퓨터를 임대하는 개념

* 인스턴스는 EC2를 생성할 때 사용하는 단위이며 1대의 컴퓨터를 의미하고 생성 시 OS 등 가상 서버 관련 설정을 선택할 수 있음

* ECS (EC2 Container Service)
  
  * EC2를 도커 컨테이너로 관리하도록 나온 서비스

* EB (Elastic Beanstalk) 
  
  * 웹 애플리케이션용 클라우드 플랫폼 서비스
  
  * 간단한 서비스 배포용으로 사용

* AWS Lamda
  
  * AWS cloud function service
  
  * 서버 없이 작성한 프로그래밍 코드를 실행하는 환경을 제공

#### S3 (Simple Stroage Service)

* 정적 요소인 이미지나 동영상을 가지고 있다가 제공

* EC2와 다르게 무제한 저장이 가능해 주로 사용

* 스냅샷 : 스냅샷을 S3에 저장된 EC2 볼륨의 백업
  
  * 스냅삿의 ID를 입력하여 스냅샷에 저장된 데이터를 사용하여 새 볼륨 만들 수 있음
  
  * 스냅샷 필드에 텍스트를 입력하여 퍼블릭 스냅샷을 검색

#### RDS

* Relational Database Service
  
  * RDBMS 클라우드 서비스
  
  * 아마존 오로라, mysql, 마리아DB, PostgreSQL, Oracle 서버등을 지원
  
  * DynamoDB : AWS의 NoSQL 데이터베이스 서비스

### EC2 서버

* EC2 콘솔에 들어오면 리소스에 아래와 같은 화면이 뜸

<img title="" src="https://github.com/Hyung-Seok/T.I.L/blob/master/Server/images/EC2.png" alt="">

* 1. Software configuration
  
  AMI(Amazon Machine Image) 는 소프트웨어 설정 탬플릿
  
  소프트웨어 구성(운영 체제, 애플리케이션 서버, 애플리케이션) 을 선택할 수 있는 단계
  
  * 루트 디바이스 유형 : ebs
  
  * 가상화 유형 : hvm
  
  * ENA 활성화 : y/n
