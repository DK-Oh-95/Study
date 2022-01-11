# [Python]


## Python 특징

- **"인터프리터 언어(interpreter)"**
  - 소스 코드를 컴파일하지 않고, 한 줄씩 소스코드를 읽어서 바로 실행
  - 컴파일 언어에 비해 느릴 수 있지만 빌드 과정이 없이 바로 실행 가능함
- **"객체 지향 프로그래밍(Object Oriented Programming)"**
  - 파이썬은 모두 객체로 이뤄져 있음
- **"동적 타이핑(Dynamic Typing)"**
  - 변수에 별도의 타입 지정이 필요없음

  
## Python 개발환경

- 대화형 환경
  - Python 기본 Interpreter : 기본적으로 활용 가능하나 디버깅 및 코드 편집, 반복실행 어려움
  - Python Jupyter Notebook : 웹 브라우저 환경에서 코드를 작성할 수 있는 오픈소스
- 스크립트 실행
  - .py 파일을 작성하고 IDE(pycharm) 혹은 Text editor(VS code) 활용

- docstring : 특수한 형태의 주석, 여러 줄 주석도 가능하지만 주로 함수/클래스의 설명을 작성
  - """ docstring

    함수나 클래스의 기능을 설명"""

- 표현식(expression)
  - 평가(evaluate)되고, 값으로 변경
  - 하나의 값으로 환원(reduce)될 수 있는 문장
  - 식별자, 값, 연산자로 구성

- 문장(statement)  : 파이썬은 1줄에 1문장이 원칙
  - 실행 가능(executable)한 최소한의 코드 단위
  - 모든 표현식은 문장 : 표현식이 아닌 문장이 존재함 ex) del
  
- 이스케이프 시퀀스(escape sequence)
  - \n : 줄바꿈, \t  : 탭, \r : 캐리지리턴, \0 : null, \\\ : \ , \\' : ' , \\" : "

- sequence : string, tuple, list, range
  - 순서대로 != 정렬된 것
  
- iterable : 순회가능한 (for문은 순회 가능한 객체의 요소를 모두 순회한다)

![image-20210724175201114](C:\Users\오동근\AppData\Roaming\Typora\typora-user-images\image-20210724175201114.png)

- 딕셔너리(dictionary) : key와 value가 쌍으로 이뤄진 자료구조
  - key는 변경 불가능한 데이터(immutable)만 활용 가능
    - string, integer, float, boolean, tuple, range
  - value는 모든 값으로 설정 가능 (리스트, 딕셔너리 등)

- 변경 불가능한 데이터(immutable)
  - 리터럴(literal) - 숫자(number), 문자열(string), 참/거짓(boolean)
  - range
  - tuple

- 변경 가능한 데이터(mutable)
  - list
  - set
  - dictionary

![image-20210725010415548](C:\Users\오동근\AppData\Roaming\Typora\typora-user-images\image-20210725010415548.png)


![image-20210807134552655](C:\Users\오동근\AppData\Roaming\Typora\typora-user-images\image-20210807134552655.png)

---

- parameter (매개변수) : 함수에 입력으로 전달된 값을 받는 변수

  - ```python
    def my_func(a,b):
        pass
    ```
  
- argument({전달}인자, 인수) : 함수를 호출할 때 함수에 전달하는 입력 값

  - ```python
    my_func(1, 2)
    ```

- list 주소가 아닌 값만 복사하는법
  - a = [1, 2, 3]
  - b = [:]

- 가변인자 수업자료 잘못된 부분 : .items() 추가해야 한다. 아니면 value 못 받아옴

  - ```python
    def my_func(**kwargs):
        for key, value in kwargs.items():
            print(key, value)
            
    my_func(a=100, b=89, c=88)
    ```

- 가번 인자 리스트(Arbitrary Argument Lists)
  - 함수가 임의의 개수 인자로 호출될 수 있도록 지정
  - 인자들은 튜플로 묶여 처리되며, 매개 변수에 *을 붙여 표현
    - *args : arguments라는 의미로 함수 호출 시 여러 인자들을 사용할 수 있다.

- 가변 키워드 인자(Arbitrary Keyword Arguments)
  - 함수가 임의의 개수 인자를 키워드 인자로 호출될 수 있도록 지정
  - 인자들은 딕셔너리로 묶여 처리되며, 매개변수에 **를 붙여 표현
    - **kwargs : Ketword arguments라는 의미로 함수 호출 시 Key = 'value' 형태로 여러 인자를 사용할 수 있다.

- 변수 수명주기(lifecycle)
  - 빌트인 스코프(built-in scope) : 파이썬이 실행된 이후부터 영원히 유지
  - 전역 스코프(global scope) : 모듈이 호출된 시점 이후 혹은 인터프리터가 끝날때까지 유지
  - 지역 스코프(local scope) : 함수가 호출될 때 생성되고, 함수가 종료될 때까지 유지

![image-20210725154607895](C:\Users\오동근\AppData\Roaming\Typora\typora-user-images\image-20210725154607895.png)


## 얕은복사(Shallow Copy) vs 깊은복사(Deep Copy)

- 얕은 복사 : 배열의 주소값만 복사
- 깊은 복사 : 새로운 배열을 만들어서 값을 그대로 복사

---


## 모듈(07/28)

- PSL(Python Standard Library)

- pip(python package ---)
- 


## OOP

- 객체


