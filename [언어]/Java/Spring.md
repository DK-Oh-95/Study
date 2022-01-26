# [Spring]



## Back-End (Servlet & JSP)



#### APACHE

- Apache HTTP Server
- 아파치 소프트웨어 재단에서 만든 웹서버 프로그램
  - "웹서버"
    - 하드웨어 분야 : 웹 서버 소프트웨어와 웹 사이트의 구성 요소 파일을 저장하는 컴퓨터
      - ex) HTML 문서, 이미지, CSS 스타일시트 및 JavaScript 파일
    - 소프트웨어 분야 : HTTP 서버. URL(웹주소) 및 HTTP(프로토콜 주소)를 이해하는 소프트웨어
- 클라이언트에서 요청하는 HTTP 요청을 처리하는 웹서버
  - Static type(HTML, CSS, 이미지 등)의 데이터만을 처리하기 때문에 톰캣 등장



#### Tomcat(톰캣)

- WAS(Web application server) (컨테이너, 웹 컨테이너, 서블릿 컨테이너로도 불림)
- 웹 서버와 연동하여 실행할 수 있는 자바 환경 제공
  - 자바서버페이지(JSP)와 자바 서블릿이 실행할 수 있는 환경 제공
- JSP와 Servlet을 구동하기 위한 서블릭 컨테이너 역할
  - 컨테이너 : 동적 데이터를 가공하여 정적 파일로 만들어주는 모듈
- 아파치서버와는 다르게 DB연결, 다른 응용프로그램과 상호 작용 등 동적인 기능 사용 가능



#### Servlet

- 클라이언트의 요청을 처리하여 결과를 제공하는 자바 인터페이스
  - Servlet Contaioner
    - 서블릿들을 모아 관리
    - 새로운 요청이 들어올 때마다 새로운 스레드 생성
    - 작업이 끝난 서블릿 스레드 자동 제거
  - `@WebServlet("/")`
    - annotation : url상에서의 mapping
    - 해당 서블릿을 웹에서 호출할 수 있는 키워드
- Web Architecture
  1. Web Server
     - 요청(request)을 받고
     - 응답(response)을 준다
  2. Web Browser
     - 요청 및 data 발생
  3. Application Server
     - Web과 합쳐서 WAS(Web Application Server, ex.Tomcat)라 표현
       - Web에서 java를 돌아가게 >> servlet
     - web과 RDBMS의 중간에서 date 작업 logic 처리
     - Presentation
       - 작업의 결과물 (html, XML)
     - Business Logic
     - Persistence Logic (DB Logic)
  4. RDBMS
     - Application Server의 Persistence Logic과 상호작용
     - JDBC 사용



#### IoC (Inversion of Control) & DI (Dependency Injection)



- "IoC, 제어의 역전"
  - 객체(<u>Bean</u>) 생성과 객체간 의존관계의 제어권이 개발자가 아닌 IoC Container에서 관리
  - 객체를 생성하면 스프링에서 스캔하여 메모리에 주입한다.



- "DI, 의존성 주입"

  - 각 객체간의 의존성을 컨테이너가 자동으로 연결
  - 스캔한 객체를 모든 클래스의 메서드에서 공유해서 사용 가능

  1. **Setter Injection**
     - 인자(argument)가 없는 생성자를 사용하여 객체 생성 후 setter 메서드를 사용해 의존성 주입, <property/> element 사용
  2. **Constructor Injection**
     - 인자를 가지고 있는 생성자를 사용하여 의존성 주입, <constuctor-arg/> element 사용









---



# [Spring Boot]



#### 개발환경 설정



- 필요 사항

  1. JDK 설치

     - 자바 코드의 번역과 실행을 담당하는 실행 도구
     - `adoptopenjdk`설치 (가장 많이 쓰이는 8버전)
  2. IDE 설치
  
     - 개발 생산성 향상
  3. Springboot 프로젝트

     - spring initializer 사이트에서 생성
     - **"Artifact"** : 생성할 프로젝트 명
     - **"Dependencies"** : 스프링부트 프로젝트에 필요한 여러 도구들 추가
       - <u>Spring Web</u> : 웹 프로젝트 도구
       - <u>H2 Database</u>
       - <u>Mustache</u> : 화면 생성 도구(view templates)
       - <u>Spring Data JPA</u> : DB 편리성 향상 도구
  



#### View Templates & MVC pattern



- **"View Templates"**
  - 웹페이지의 변수를 활용
  - 화면 담당 - 웹페이지를 하나의 틀로 만들고 각 요소에 변수를 입력하도록 설계
  - **"Controller"**
    - logic - 처리과정 담당
  - **"Model"**
    - data - 데이터 담당

- **"MVC pattern"**
  - 분야별 담당자 분리 
  - Model / View / Controller 각 담당자 분리
  - View
    - `src/main/resources/templates` 위치에 생성







