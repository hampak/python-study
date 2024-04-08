## 변수

> 변수는 특정 값을 저장하기 위해 사용되는 **식별자**를 말한다. 또한, 언제든지 새로운 값을 할당할 수 있다.

변수 식별자 이름을 지정하는 데에 몇 가지 규칙이 있다.

1. 파이썬 키워드 식별자는 식별자로 사용할 수 없다. (이미 파이썬에서 사용되는 명령어 이름 등을 사용할 수 없음)
2. 영문자는 대/소문자를 구분한다.
3. 식별자 구성은 영문자, 숫자, 밑줄문자(_)로 이루어진다.
4. **첫 글자는 반드시 영문자나 밑줄(_)로 시작해야 한다.**
5. 식별자 중간에 공백을 포함할 수 없다.
6. 식별자 생성에 길이 제한은 없다.

![IMG_A2276FFE1A3B-1](https://github.com/hampak/python-study/assets/85291626/6cb3e27a-6e47-49b2-8476-a98aa6cc72f2)

변수에 값을 할당하는 것을 "변수에 값을 할당" 혹은 "변수를 * 값으로 초기화"라고 표현한다.

변수에 값을 할당한 후, 프린트 문에 사용할 수 있다.

```py
name = "Javascript"
print("I love", name)
# I love Javascript
```

## format() 함수

함수 중에 `format()`이라는 **문자열 포맷팅 함수**를 통해 숫자의 가독성을 높일 수 있다.

> {형식규칙:,}.format(값) 으로 이루어져 있다.

예를 들어,

```py
pay=2000000
bonus=40000
salary=pay+bonus
print("My base salary is {0:,} / bonus pay is {1:,} / and monthly salary is {2:,}".format(pay, bonus, salary))
# My base salary is 2,000,000 / bonus pay is 40,000 / and monthly salary is 2,040,000
```

## 정수형 숫자 자리 형식 지정

- 형식규칙에 콜론(:) 앞 숫자는 출력 순서를 나타낸다.
- `n`은 출력되는 수의 자리수를 의미한다.
- `d`는 "정수형 유형 숫자"를 의미한다 (여기에 실수를 넣으면 오류 발생)

> {순서:*n*d}.format(변수)

예를 들어,

```py
num1 = 100
num2 = 200
num3 = 300
print("{0:d} {1:5d} {2:05d}".format(num1, num2, num3))
# 100   200 00300
# 100 VV200 00300
```

