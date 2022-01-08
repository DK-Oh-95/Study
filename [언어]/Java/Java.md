# [Java]

#### Java 특징

- **"객체지향 언어"**
  - 객체 : 멤버 변수, 메서드를 가진다
  - 속성 : 괄호 없는 것 / 메서드 : 괄호 있는 것
  - ex) System."out"(속성)."println()"(메서드)  

- **"Write Once, Run Anywhere"**
  - **바이트코드** (C++은 바이너리코드)
  - 운영체제에 종속적이지 않다
  - JVM에서 동작
    - Java Virtual Machine

- **"Garbage Collection"**
  - 더 이상 사용하지 않는 메모리를 자동으로 정리하는 기능
  - C에서는 쓰레기 메모리 수거해줘야 함
  - 언제 발생하는지 정확히 알 수는 없음(언젠가 일어남)
  - 메모리 관리할 필요가 없는 것이 매우 큰 장점

- 파일 저장명은 public 클래스명으로 저장
  - .java 확장자
  - console 실행 명령어
    - compile: "javac -d . (파일명.java)"
    - run: "java (package명.클래스명)"
    
- Class
  - 자바프로그래밍 최소 단위

- **"Variable"**
  - 메모리 공간, 그릇
  - 메모리 공간에 값(value)을 할당(assign) 후 사용
  - 공간의 크기는 타입별로 달라짐

- **"Type"**
  - 변수에 저장되는 데이터의 종류
  - **Primitive Type(기본형)**
    - 미리 정해진 크기의 Memory Size로 표현
    - 변수 자체에 값 저장
    - 논리형
      - boolean
    - 정수형
      - byte : 8bit
      - short : 16bit
      - int(default) : 32bit
      - long : 64bit
    - 실수형
      - float : 32bit
      - double(default) : 64bit
    - 문자형
      - char : 16bit
  - **Reference Type(참조형)**
    - 미리 정해질 수 없는 데이터의 표현
    - 변수에는 실제 값을 참조할 수 있는 주소만 저장

- local 변수는 사용전에 초기화 필요

- "final"
  - ex) final int i = 0;
  -    i = 10
  - final로 정의한 변수는 변경 불가
  - blank 상태면 가능
  - ex) final int i;
  -    i = 10

- 형변환(Type casting)
  - primitive는 primitive끼리, reference는 reference끼리 변환 가능
  - 다른 타입 변환을 위해 Wrapper 클래스 사용
  - "명시적 형변환"
    - 큰집 → 작은집 
    - 데이터 손실 있음
    - byte b = (byte) i; 
      - 형변환 연산자 필요
  - "묵시적 형변환"
    - 작은집 → 큰집
    - 데이터 손실 없음
    - long이 64bit이고 float이 32bit이지만 타입의 크기가 아닌 타입의 표현 범위가 커지는 방향으로 할당
