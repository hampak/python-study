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


# 만약, print("넓이:", result) 라 했으면 에러 없음
```


















