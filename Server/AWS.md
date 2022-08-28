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

* Software configuration
  
  AMI(Amazon Machine Image) 는 소프트웨어 설정 탬플릿
  
  소프트웨어 구성(운영 체제, 애플리케이션 서버, 애플리케이션) 을 선택할 수 있는 단계
  
  * 루트 디바이스 유형 : ebs
  
  * 가상화 유형 : hvm
  
  * ENA 활성화 : y/n

* instance type
  
  * 해당 단계에서 CPU, 메모리, 스토리지 등 하드웨어적인 부분과 네트워크 용량 조합을 선택할 수 있음
  
  * instance type 을 눌러보면 general purpose, compute/memory/storage/optimized 혹은 GPU instance 등으로 나눌 수 있음

* instance detail
  
  * 인스턴스의 세부적인 내용에 대해서 설정, 검토 및 시작 버튼 생성됨
  
  * Auto scaling : 트래픽에 따라 EC2 인스턴스들을 자동으로 확장/삭제해주는 서비스
  
  * 스팟 인스턴스 : EC2 스페어 용량의 수요, 공급에 따라 가격이 결정되어 on-demand 요금보다 절감된 비용으로 서버를 사용할 수 있음
  
  * 내가 제시하는 가격보다 스팟 시장 가격이 낮으면 인스턴스가 시작되고, 반대로 스팟 시장 가격이 높으면 인스턴스가 종료

* 보안그룹 구성
  
  * 보안그룹에서 프로토콜이나 리소스, 포트 등을 선택해서 어떤 트래픽이 인스턴스에 도달할 수 있는지에 대한 규칙을 정함
  * 인터넷 트래픽을 인스턴스에 도달하도록 하는 경우 HTTP, HTTPS 트래픽을 허용하고, 어떤 전송 방식을 사용할지, 어떤 포트를 통해 접속할지에 대해 정할 수 있음

* 프로토콜
  
  * 기본적으로 통신 규약을 뜻함
  
  * 네트워크는 정말 다양한 컴퓨터로 구성되어 있기 떄문에 네트워크간 공통으로 사용할 수 있는 규약이 필요
  
  * AWS에서 보안그룹을 선택할 때 유형과 프로토콜이 따로 나뉘어져있는 것을 볼 수 있음
