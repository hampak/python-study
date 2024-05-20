## 함수

파이썬에서 함수는 다음과 같이 선언 및 호출한다:

```py
def 함수이름(): # 함수 정의/선언
  함수 본문 # 함수 호출되었을 때 실행되는 문

함수이름() # 함수 호출
```

간단한 연습을 위해 "사용자의 이름과 나이를 물어보고 출력하는 함수"를 만들어 보면 이렇다:

```py
def myFunction():
  name = input("이름: ")
  age = int(input("나이: "))
  print("이름은 {}이고 나이는 {}세 입니다.".format(name, age))

myFunction()

# 이름: John
# 나이: 25
# 이름은 John이고 나이는 25세 입니다.
```

또 다른 문제를 풀어보자. 원하는 구구단을 출력하는 프로그램이다:

```py
def multiply():
  num = int(input("원하는 구구단: "))
  for i in range(1, 10):
    print(f"{num} * {i} = {num * i}")

multiply()

# 원하는 구구단: 5
# 5 * 1 = 5
# 5 * 2 = 10
# 5 * 3 = 15
# 5 * 4 = 20
# 5 * 5 = 25
# 5 * 6 = 30
# 5 * 7 = 35
# 5 * 8 = 40
# 5 * 9 = 45
```

## 인자와 매개변수

- 인자(argument)란 함수 호출 시 데이터와 함께 함수를 호출할 수 있는데 이 때 사용되는 데이터 값을 인자라고 한다.
- 매개변수(parameter)란 함수 정의 프로그램에서 전달받은 값으로, 호출 당시 인자 순서대로 차례로 매개변수로 넘겨진다.

```py
def nameOfFunction(parameter1, parameter2):
  #

nameOfFunction(argument1, argument2)
```

매개변수와 인자를 이해하기 위해 간단한 코드를 짜보자:

```py
def sum(num1, num2):
  print("{} + {} = {}".format(num1, num2, num1 + num2))

a = 10
b = 20
sum(a, b)
# sum(a = 10, b = 20) 도 가능

# 10 + 20 = 30
```

인자값을 리스트 자체로도 넘길 수 있다:

```py
def sumOfList(list):
  sum = 0
  for i in list:
    print(i)
    sum += i
  print("합 = {}".format(sum))

l = [1, 2, 3, 4, 5]
sumOfList(l)

# 1
# 2
# 3
# 4
# 5
# 합 = 15
```

### 간단한 실습

> 함수 호출 영역에서 팩토리얼 값을 입력 받아 인자 값으로 함수를 호출한다. 함수 정의 영역에서 팩토리얼 값을 구한 후, 결과 값을 반환하여 다음과 같이 출력되도록 코드를 작성하라

```
어떤 숫자: 5
5! = 120
```

```py
def factorial(n):
  sum = 1
  for i in range(5, 0, -1):
    sum *= i
  return sum

num = int(input("어떤 숫자: "))
result = factorial(num)
print("{}! = {}".format(num, result))

# 어떤 숫자: 5
# 5! = 120
```

---

## 내장함수

파이썬 내장함수란, 파이썬을 설치하게 되면, 파이썬에 처음부터 포함이 되어 있어서 기본적으로 사용할 수 있는 함수이다. 또한, 내장함수는 `import` 선언 없이 바로 사용이 가능하다.

![IMG_242A7CF580F6-1](https://github.com/hampak/python-study/assets/85291626/eb61fac3-c75c-4527-9583-d5a5f2052c16)


### 내장함수: 수학함수 `math()`

- 수학함수를 사용을 위해 `import math`를 포함해야 한다.
- 수학 함수들은 소수 첫째자리에서 연산을 수행한다.

  
`ceil(x)` 함수는 무조건 올려서 출력하는 함수이다.

```py
import math

x = 2.487
y = -2.1345

print(math.ceil(x))
print(math.ceil(y))

# 3
# -2
```

`floor(x)` 함수는 무조건 내려서 출력하는 함수이다.

```py
import math

x = 2.487
y = -2.1345

print(math.floor(x))
print(math.floor(y))

# 2
# -3
```

`trunc(x)` 함수는 무조건 절삭시키는 함수이다.

```py
import math

x = 2.487
y = -2.1345

print(math.trunc(x))
print(math.trunc(y))

# 2
# -2
```












