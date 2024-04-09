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












