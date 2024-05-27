## 복합대입연산자

복합대입연산자는 산술연산자와 대입연산자를 합쳐 놓은 연산자로, 코드를 조금이나마 더 간결하게 해준다. 복합대입연산자는 다음과 같다:

![IMG_63E6D459F252-1](https://github.com/hampak/python-study/assets/85291626/a9d762a6-d3a6-497d-9930-8e0b8560fcd3)

**`=`는 항상 오른쪽에 있다!!**

코드를 작성해보자:

```py
a = 10 #a를 10으로 초기화한다.
a += 5
print(a)
# 15
```

파이썬에서는 복합대입연산자를 이용하여 문자열 출력도 가능하다. 다음과 같이 할 수 있다:

```py
str1 = "Javascript"
str2 = "is"
str3 = "a"
str4 = "lovely"
str5 = "language."
result = ""
space = " "
result += str1 + space
result += str2 + space
result += str3 + space
result += str4 + space
result += str5 + space
print(result)
# Javascript is a lovely language.
```

## 관계연산자

관계연산자는 대소 크기를 비교하는 연산자이다.

![IMG_C5ED7C20AC51-1](https://github.com/hampak/python-study/assets/85291626/459d91b9-e0ef-43a3-a63b-0ad90bd52f1f)

관계연산자는 **True** 혹은 **False**를 리턴한다.

```py
a = 10
b = 5
print(a > b)
# True
```

## 논리연산자

논리연산자는 연산 결과에 따라 참인지 거짓인지를 판단한다.

![IMG_EC295522DCA9-1](https://github.com/hampak/python-study/assets/85291626/3f8fbf09-1a3c-4e8e-8839-a8428389d011)

논리연산자 또한 **True** 혹은 **False**를 리턴한다.

### and

`and`연산자는 조건 모두가 참이어야 True를 반환한다.


### or

`or`연산자는 조건 중 하나만이라도 참이면 True를 반환한다.


### not

`not`연산자는 (예를 들어) a가 거짓이면 True를 반환하고 a가 참이면 False를 반환한다.


```py
a = 100
b = 200

print(a < b and a == 110)
# False

print(a < b or a == 110)
# True

print(not a) # 정수형 숫자는 True 값이다
# False
```

## 간단한 연습

> 각 과목 점수는 다음과 같다. 각 과목 모두 80점이 이상인지 판별하여 논리 연산자를 사용하여 출력하시오.

`kor = 90 // eng = 80 // math = 100`

```py
kor = 80
eng = 90
math = 100

result = (kor >= 80) and (eng >= 80) and (math >= 80)

print(result)
# True
```

---

## 삼항연산자

자바스크립트의 ternary operator와 비슷하다. 복잡한 if ~ else 조건문을 삼항 연산자로 사용하게 되면 코드를 더욱 간결하고 빠르게 작성할 수 있다.

![IMG_7FB20086FD95-1](https://github.com/hampak/python-study/assets/85291626/ad302bd0-5ea5-4a8a-ae73-b9e471f75d01)


간단한 연습을 해보자:

```py
num1 = 125
num2 = 100
num3 = 120

max = num1 if num1 > num2 else num2
max = num3 if num3 > max else max

print(max)
# 125
```

## 간단한 연습

> 사용자로부터 어떤 숫자 하나를 입력 받아, 입력한 숫자가 3의 배수인지를 판별하는 프로그램을 삼항 연산자를 이용하여 작성하시오.

```py
num = int(input("숫자를 입력하시오:"))

result = (f"당신이 입력한 숫자{num}은 3의 배수입니다.") if num % 3 == 0 else (f"당신이 입력한 숫자{num}은 3의 배수가 아닙니다.") 

print(result)

# 숫자를 입력하시오:24
# 당신이 입력한 숫자24은 3의 배수입니다.
```

> 사용자로부터 물건 가격을 입력받아, 물건 가격이 6만원 이상인 경우 할인 대상에 포함될 수 있는지를 판별하는 프로그램을 삼항 연산자를 이용하여 작성하시오

```py
price = int(input("가격을 입력하시오: "))

result = True if price >= 60000 else False

print(result)

# 가격을 입력하시오: 10000
# False
```

> 사용자로부터 나이를 입력 받아, 영화를 볼 수 있는 등급인지를 판별하는 프로그램을 삼항 연산자를 이용하여 작성하시오

```py
age = int(input("나이를 입력하시오: "))

result = "이 등급의 영화를 시청할 수 있습니다" if age >= 17 else "이 등급의 영화를 시청할 수 없습니다."

print(result)

# 나이를 입력하시오: 18
# 이 등급의 영화를 시청할 수 있습니다
```




















