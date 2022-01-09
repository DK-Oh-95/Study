# [Eclipse]

#### IDE, Integrated Development Environment

- 통합 개발 환경
- 소스 편집기는 기본이고, 컴파일러, 디버거, 유닛테스트와 같은 개발에 필요한 다양한 도구들이 결합되어 있는 소프트웨어


#### Eclipse 특징

- **"View"**
  - 각각의 작업 창

- **"Perspective"**
  - "관점"
  - View의 모임
  - 어떤 관점에서 프로젝트 바라볼 것인가
  
- **"build path"**
  - JRE 라이브러리 이외의 사용할 라이브러리

- 모든 운영체제 지원


#### 실행 순서

###### 1. 프로젝트 생성
- Package Explorer에서 우클릭 → 프로젝트명, 위치 지정 후 생성
- bin 폴더 생성
  - binary 파일
  - .class 파일들 저장 (컴파일 된 파일)
- src 폴더 생성
  - source 파일
  - .java 파일들 저장 (내가 작성한 코드)
- .classpath / .project 파일 생성
  - 해당 프로젝트에 대한 정보 저장

###### 2. Package 생성
- 생성한 프로젝트 우클릭 → New → Package
- 파일 구분을 위한 디렉토리 개념
- 다른 개발자와 중복될 가능성을 낮추기 위해 도메인 주소 사용 

###### 3. Class 생성
- 생성된 package 우클릭 → New → Class
- package에 소속된 java 파일 생성
- 이름 작성 후 public static void main(String[] args) 체크
- 코드 변경 후 저장(ctrl+s)하면 자동으로 컴파일
  - bin 폴더 내부에 .으로 디렉토리 구분한 package 주소 안에 저장

#### 단축키

- "sysout + ctrl + space"
  - System.out.println()