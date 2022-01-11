# [Git]


## 1. 버전 관리

- 버전 관리 시스템 (VCS, Version Control System)
  - 파일 변화를 시간에 따라 기록, 특정 시점 버전 관리
  - **"로컬 버전 관리"**
    - 간단한 데이터베이스를 사용해서 파일의 변경 정보 관리
    - ex) RCS(Revsion Control System)
    - ![img.png](./img/img.png)
  - **"중앙집중식 버전관리 (CVCS, Central VCS)"**
    - 별도의 파일 관리 서버
    - 클라이언트가 중앙 서버에서 파일 받아서 사용(Checkout)
    - 단점
      - 중앙 서버에 문제 발생 시 업무 및 백업 불가
    - ![img_1.png](img_1.png)
  - **"분산 버전 관리 시스템 (DVCS)"**
    - Git, Mecuial, Bazaar, Darcs 등
    - 저장소를 히스로티와 더불어 전부 복제
      - 서버에 문제 발생 시 복제물로 다시 작업 가능
      - 클라이언트 중 아무거나 사용해서 백업 가능
    - ![img_2.png](img_2.png)


## 2. Git 기초

- 기존 디렉토리 Git 저장소로 만들기
  - 사용할 프로젝트 디렉토리로 이동
  - `git init`
    - .git이라는 하위 디렉토리 생성
    - 저장소에 필요한 Skeleton 파일 생성
  - 저장소에 파일 추가 및 커밋
    - `git add *.c`
    - `git commit -m 'first commit`

- 기존 저장소 Clone하기
  - 



- 출처 : https://git-scm.com/book/ko/v2