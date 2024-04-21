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
- `d`는 "정수형 유형 숫자"를 의미한다 (여기에 실수를 넣으면 오류 발생 - 참고로 실수를 포맷팅 하고 싶다면 `f`를 사용)

> {순서:*n*d}.format(변수)

예를 들어,

```py
num1 = 100
num2 = 200
num3 = 300
print("{0:d} {1:5d} {2:05d}".format(num1, num2, num3))
# {2:05d}에서 "0"은 남은 자리를 0으로 채우라는 뜻이다.

# 100   200 00300
# 100 VV200 00300
```

## 실수형 숫자 자리 형식 지정

이와 비슷하게 **실수형** 숫자로 포맷팅 할 수 있다.

- 형식규칙에 콜론(:) 앞 숫자는 출력 순서를 뜻한다.
- `0,`의 의미는 "정수형 숫자로 3자리마다 쉼표를 부여하라"의 뜻이며 `0`은 생략 가능하다.
- `.숫자f`는 실수형 소숫점 자리르 나타낼 때 사용된다.

> {0:0,.1f}.format(값)

예를 들어,

```py
num1 = 56700000
num2 = 100000.415234
print("{0:0,.2f} {1:0,.3f}".format(num1, num2))
# 56,700,000.00 100,000.415
```

## f-string format

f-string format은 문자열을 아주 간결하게 출력할 때 사용하기 편리하다. 용법은 다음과 같다:

> f"string goes here".format(var)"

이것을 활용해보면 다음과 같다:

```py
name = "John"
age = 25 # 여기서 "age" 변수는 문자열이다
print(f"My name is {name} and I'm {age} years old.")
# My name is John and I'm 25 years old.
```

## input 함수

**input()** 함수는 사용자가 키보드로부터 입력한 데이터를 가져오는 함수이다.

> x = input() // x 변수에 인풋 함수로부터 입력받은 값으로 초기화 한다

`input()`함수로 문자열을 입력받을 수 있다. 예를 들어,

```py
name = input("What's your name: ")
age = input("How old are you: ")
print("Your name is", name, "and you are", age, "years old")

# What's your name: John
# How old are you: 25
# Your name is John and you are 25 years old
```

이와 다르게 `input()`함수는 숫자형 데이터를 입력 받을 수 있다. 예를 들어,

```py
num1 = int(input("Please enter first integer: "))
num2 = int(input("Please enter second integer: "))
total = num1 + num2
print(f"{num1} + {num2} equals {total}")

# Please enter first integer: 25
# Please enter second integer: 34
# 25 + 34 equals 59
```

만약, 실수형 숫자 데이터를 입력받고 싶다면 `int` 대신에 `float`를 사용하면 된다. **`int`와 `float`는 각각 입력받은 문자열 데이터를 respective한 숫자형 데이터로 변환해준다.**


## 여러 데이터 입력받기

`input()`함수를 `.split()`함수와 같이 사용하면 여러 데이터 값을 입력받을 수 있다. 예를 들어,

```py
name = input("What's your name: ")
year, month, day = input("Please enter your date of year, month, and day in order: ").split()
print(f"Hello, {name}. You were born in the year {year}, of {month} {day}.")

# What's your name: John
# Please enter your date of year, month, and day in order: 1999 May 1
# Hello, John. You were born in the year 1999, of May 1.
```

- `.split()`함수 안에 아무 내용을 입력하지 않고 비워둔다면 **공백으로 데이터를 처리하겠다는 의미이다**.

### 간단한 연습

> 사용자로부터 숫자 3개를 입력 받아 합을 구하는 프로그램을 작성하시오.

```py
# Solution
int1 = int(input("첫 번째 정수: "))
int2 = int(input("두 번째 정수: "))
int3 = int(input("세 번째 정수: "))
print(f"{int1}와 {int2}와 {int3}의 합은 {int1 + int2 + int3} 입니다.")

# 첫 번째 정수: 150
# 두 번째 정수: 350
# 세 번째 정수: 500
# 150와 350와 500의 합은 1000 입니다.
```
