## 지역변수 (Local Variable)

- 함수가 호출되었을 때 생성되어 함수가 종료되면 사라지는 변수
- 함수 내에서만 해당 변수로만 사용할 수 있으며, 해당 지역을 벗어나면 자동으로 소멸되는 변수
- 함수 바깥에서는 지역변수를 사용하여 접근할 수 없음

```py
def greet():
  name = "홍길동"
  print("Hello", name)

greet()

# Hello 홍길동
```

```py
def add(x, y):
  sum = x + y
  print("SUM:", sum)

add(10, 20)

# SUM: 30
```

만약, `sum` 변수를 그 함수 밖에서 사용을 하고 싶다면 `return`하면 된다.

```py
def add(x, y):
  sum = x + y
  return sum

print("SUM:", add(10, 20))

# SUM: 30
```

다음 코드는 에러를 발생시킨다:

```py
def rect(b, h):
  b = 10   # 지역변수
  h = 30   # 지역변수
  w = b * h   # 지역변수
  return w

base = int(input("base:"))
height = int(input("height:"))
result = rect(base, height)
print("넓이:", w)

# base:10
# height:20
# Traceback (most recent call last):
#   File "/Users/haeminpark/Desktop/code/hufs/computational-thinking/index.py", line 10, in <module>
#     print("넓이:", w)
# NameError: name 'w' is not defined --> because "w" is a local variable!


# 만약, print("넓이:", result) 라 했으면 에러 없음 --> 결과는 "300"을 리턴함
```

**위 예시는 고치면 `300`을 반환한다. 이것은 전역변수가 아닌, 함수 내에서 선언된 지역변수가 우선이기 때문이다.**


### 간단한 실습

> 사용자로부터 어떤 숫자 하나를 입력 받아 함수 호출 시 인자로 사용하여 해당 숫자만큼 누적된 값을 함수 프로그램 내에서 출력하는 함수 프로그램을 작성 하시오.

```py
# 예시

숫자: 5
1 1
2 3
3 6
4 10
5 15
```

```py
def add(num):
  sum = 0
  for i in range (1, num + 1, 1):
    sum += i
    print(f"{i}", f"{sum}")

n = int(input("숫자: "))
add(n)

# 숫자: 5
# 1 1
# 2 3
# 3 6
# 4 10
# 5 15
```

> 사용자로부터 2의 지수승(거듭제곱)으로 사용할 숫자 하나를 입력 받아 함수 호출 시 인자로 사용하여 해당 숫자만큼 계산된 결과 값을 리턴하여 함수 호출 영역에서 다음과 같이 출력되도록 프로그램을 작성하시오.

```py
# 예시

원하는 지수승? 3

2 ** 3 = 8
```

```py
def exponentiation(exponent):
  base = 2
  result = 2 ** exponent
  return result

expo = int(input("원하는 지수승? "))
res = exponentiation(expo)
print(f"2 ** {expo} = {res}")

# 원하는 지수승? 3
# 2 ** 3 = 8
```

---

## 전역 변수 (global variable)




















