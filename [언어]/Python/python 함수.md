- map(함수명, 시퀀스(리스트))

  - map(int, 문자열) : 문자열에 포함된 문자 하나하나 순서대로 int() 함수 적용해라
  - 그 정보 갖고 있는 객체반환 

---

### 반복문

- while : 조건 만족할때까지 계속
  - while 조건문:

    ^^^^실행할 문장

- for : 횟수 정해져 있을 때
- break : 반복문 종료
- continue : 바로 다음 코드 블록은 수행하지 않고 다음 반복을 수행
- for-else : 끝까지 반복문을 실행한 이후에 else문 실행 (break를 통해 중간에 종료되는 경우 else문 실행 안함)

---

- enumerate(list) : 리스트를 순회하면서 (index, value) 형태의 tuple로 구성된 열거 객체를 반환

  ```python
  # start를 지정하면 해당 값부터 순차적으로 증가, 기본값은 0
  list(enumerate(members, start = 1))
  [(1, '민수'), (2, '영희'), (3, '철수')]
  ```

  

- divmod(a, b) : a 나누기 b의 몫과 나머지를 quotient, remainder에 각각 할당
  - quotient, remainder = divmod(a, b)



- pstdev : 표준편차 구하는 함수 (statistics 라이브러리 import 해야함)

---

##  데이터 구조(Data structures)

- 순서가 있는 데이터 구조 : 문자열, 리스트
- 순서가 없는 데이터 구조 : 세트, 딕셔너리

### 문자열 method(함수와 마찬가지)

- .find(x) :  문자열에서 x가 있는지 확인(있으면 처음 위치, 없으면 -1 반환)
  - 'apple'.find('p') => 1 
- .index(x) : 문자열에서 x의 첫번째 위치 반환, 없으면 오류 발생
  - 'apple'.index('p') => 1
- .replace(old, new[, count]) : 바꿀 대상 글자를 새로운 글자로 바꿔서 반환(복사본 반환), count를 지정하면, 해당 개수만큼만 시행 
  [.count] -> 대괄호로 표기하는 이유 : 배커스-나우르 표기법(BNF)에서 대괄호는 '선택적 인자'라는 뜻, 파이썬 문법이 아닌 문서 표기 시에만 사용
  - 'coone'.replace('o','a') => 'caane'
  - 'woooooowoo'.replace('o', '!', 2) => 'w!!oooowoo'
- .strip([chars]) : 특정한 문자를 지정하면, 양쪽을 제거하거나(strip), 왼쪽을 제거하거나(lstrip), 오른쪽을 제거(rstrip). 문자열을 지정하지 않으면 공백을 제거

- split(sep=None) : 문자열을 특정한 단위로 나눠 **리스트로 반환**
  - 'a_b_c'.split('_') => ['a,b,c']
  - 'a b c'.split() => ['a', 'b', 'c']
- 'separator'.join(iterable) : 반복가능한 컨테이너 요소들을 구분자(separator)로 합쳐 **문자열 반환**
  - '!'.join('ssafy') =>('s!s!a!f!y')
  - ' '.join(['3', '5']) => '3 5' : 리스트 사이에 공백 추가하여 문자열 반환



- .capitalize() : 첫 문자를 대문자, 나머지는 소문자
- .title : '나 공백 이후를 대문자로

- upper() : 모두 대문자로
- lower() : 모두 소문자로
- swapcase() : 대 <-> 소문자로 전체 변경

###### is가 붙은 함수는 true나 false를 반환한다

- isalpha() : 알파벳 문자 여부(단순 알파벳이 아닌 유니코드 상 Letter(한국어도 포함))
- isupper() : 대문자 여부
- islower() : 소문자 여부
- istitle() : 타이틀 형식 여부



### 리스트 method

- .append(x) : 리스트에 값을 추가함(하나만 추가)
- .extend(*iterable*) : 리스트에 iterable의 항목을 추가함
- .insert(i,x) : 정해진 위치 i에 값 x를 추가함, 리스트의 길이보다 큰 경우 맨 뒤에 추가
- .remove(x) : 리스트에서 값이 x인 것 전부 삭제, 없는 경우 ValueError
- .pop(i) : 정해진 위치 i에 있는 값을 삭제하고, 그 항목을 반환함, i가 지정되지 않으면 마지막 항목을 삭제하고 반환함
- .clear() : 모든 항목을 삭제
- .index(x) : x값을 찾아 해당 첫번째 index 값을 반환, 없는 경우 ValueError
- .count(x) : 원하는 값의 개수를 반환함
- .sort() : 원본 리스트를 정렬함, None 반환 / sorted() 함수의 경우 원본 변경 없이 정렬된 리스트를 반환함
- .reverse() : 순서를 반대로 뒤집음(정렬하는 것이 아님)
- List comprehension
  - [<expression> for <변수> in <iterable>]
  - [<expression> for <변수> in <iterable> if <조건식>]

###### Built-in Function

- map(function, iterable) : 순회 가능한 데이터구조의 모든 요소에 함수를 적용하고, 그 결과를 map object로 반환, 리스트 형변환을 통해 결과 직접 확인
- filter(function, iterable) : iterable 데이터구조의 모든 요소에 함수를 적용하고, 그 결과가 True인 것들을 filter object로 반환, 리스트 형변환을 통해 결과 직접 확인
- zip(*iterables) : 복수의 iterable을 모아 튜플을 원소로 하는 zip object를 반환(같은 인덱스끼리 묶어서 반환), 가장 적은 인덱스를 가진 iterable이 기준, 리스트 형변환을 통해 결과 직접 확인



### 세트(set) method

- .add(*elem*) : 세트에 값을 추가

- .update(**others*) : 여러 값을 추가
  - a.update(['a', 'b', 'c'])
- .remove(elem) : 세트에서 삭제하고, 없으면 KetError
- .discard(elem) : 세트에서 삭제하고, 없어도 에러가 발생하지 않음
- .pop() : 임의의 원소를 제거해 반환



### 딕셔너리 method

- .get(*key[,default]*) : key를 통해 value 가져옴, KeyError 발생하지 않으며, default 값을 설정할 수 있음(기본 : None)
- .pop(*key[,default]*) : key가 딕셔너리에 있으면 제거하고 해당 값을 반환, 그렇지 않으면 default를 반환, default 값이 없으면 KeyError
- .update() : 값을 제공하는 Key, value로 덮어쓴다.
  - a = {'apple' : '사'}
  - a.update(apple = '사과')  # => {'apple' : '사과'}

- .keys() : key로 구성된 결과
- .values() : value로 구성된 결과
- .items() : (key, value)의 튜플로 구성될 결과

###### Dictionary Comprehension

- {key: value for <변수> in <iterable>}
- {key: value for <변수> in <iterable> if <조건식>}

