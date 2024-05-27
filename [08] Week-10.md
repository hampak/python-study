<img width="1299" alt="image" src="https://github.com/hampak/python-study/assets/85291626/5aea59da-8a67-408b-bc46-975d5273b87a">

<img width="1322" alt="image" src="https://github.com/hampak/python-study/assets/85291626/abd005d7-5d58-4181-9ad2-5a125a5af7db">


## 리스트

리스트는 여러 개의 자료를 하나의 변수로 관리할 때 사용되는 집합이다. 리스트 내의 데이터 항목 값을 삽입, 수정, 삭제, 정렬 등을 할 수 있다.

리스트 내의 값으로 숫자형, 문자열, 참/거짓, 리스트 등을 넣을 수 있다.

파이썬의 자료형을 크게 두 가지로 나눌 수 있는데, 지금 살펴보는 리스트는 "여러 항목의 값을 저장하는 데이터 유형"의 하나이다.

![IMG_4B421EC38854-1](https://github.com/hampak/python-study/assets/85291626/79acbb43-2428-463b-a93c-30f750ae3b38)

리스트 항목을 루프하여 각각의 값을 출력해 보자:

```py
num = [10, 15, 20, 25, 30]
for i in num:
  print(i)
```

위에서 언급했듯이 리스트 내에 문자열 데이터를 저장할 수 있다. "다음 중, 문자열의 길이가 5인 단어만 출력하는 프로그램"을 작성하면 이렇댜:

```py
str = ["Korea", "Seoul", "Incheon", "Pusan", "Jeju"]

for i in str:
  if len(i) == 5:
    print(i)

# Korea
# Seoul
# Pusan
```

### 간단한 실습

> 리스트 변수 `num = [1, 2, 3, 3, 4, 5, 6, 7, 2, 3, 8, 9, 10]` 에 숫자 항목이 저장되어 있다. [실행 결과]와 3의 개수를 구하여 출력하시오. 실행 결과 = "3의 개수 = 3개"

```py
num = [1, 2, 3, 3, 4, 5, 6, 7, 2, 3, 8, 9, 10]

count = 0

for i in num:
  if i == 3:
    count += 1

print(f"3의 개수 = {count}개")
# print("3의 개수 = {}개".format(count))

# 3의 개수 = 3개
```

> 리스트 변수 `num = [15, 23, 18, 47, 23]`에 숫자 항목이 저장되어 있다. 다음과 같이 각 항목 데이터에 따른 홀수 개수, 짝수 개수를 출력하시오.

> 홀수 개수 = 4개
> 짝수 개수 = 1개

```py
num = [15, 23, 18, 47, 23]

even = 0
odd = 0

for i in num:
  if (i % 2 == 0):
    even += 1
  else:
    odd += 1

print("홀수 개수 = {}개".format(odd))
print(f"짝수 개수 = {even}개")

# 홀수 개수 = 4개
# 짝수 개수 = 1개
```

----

## 리스트 활용

리스트를 생성하는 방법은 몇 가지가 있다.

```py
# 빈 리스트 생성하기
numList = []
print(numList)

# 리스트 생성 내장함수 사용하기
strList = list()
print(strList)

# []
# []
```

## append()

`append()` 함수를 사용하게 되면 리스트 **맨 끝**에 새로운 항목을 추가할 수 있다.

![IMG_3883E26F773B-1](https://github.com/hampak/python-study/assets/85291626/b9700369-882d-46f4-9ceb-e5f7fb27a9c0)

```py
num = []
print(num)

num.append(10)
num.append(20)
print(num)

num.insert(3, 30)
print(num)

# []
# [10, 20]
# [10, 20, 30]
```

## extend()

`extend()`를 사용하면 리스트를 확장할 수가 있다.

![IMG_2DEF7FB24802-1](https://github.com/hampak/python-study/assets/85291626/ce72ea1c-8cd2-4809-83b5-64ccf6e1ea28)

```py
numA = [1, 2, 3]
numB = [10, 20, 30]
numC = numA + numB
print(numC)

numA.extend(numB)
print(numA)

# [1, 2, 3, 10, 20, 30]
# [1, 2, 3, 10, 20, 30]
```

## 리스트 슬라이싱(slicing)

파이썬에서 슬라이싱은 리스트에서 한 번에 여러 개의 함옥을 범위를 지정하여 추출하는 기법으로 문자열, 리스트, 튜플과 같은 객체로부터 데이터 값을 가져올 수 있다. 리스트를 추출하기 위해서는 `[]` 대괄호 안에 숫자와 콜론 기호(:)를 이용한다.

![IMG_D5D795B9F68B-1](https://github.com/hampak/python-study/assets/85291626/f7ffa825-07d4-4353-b27b-003c52cd613a)

![IMG_A5C8C23D82C8-1](https://github.com/hampak/python-study/assets/85291626/4bf8f6f6-d94d-4e0d-88e0-b7f765807af4)

리스트에서 원하는 범위를 지정하기 위해서는 인덱스 번호를 사용한다.

![IMG_89D77AF8D0B1-1](https://github.com/hampak/python-study/assets/85291626/e500adab-e922-42f2-92aa-8aa3a20a3d86)


리스트 슬라이싱은 특정 범위에 해당하는 데이터 값을 추출하는 것이다.

![IMG_3944EC8DBFD2-1](https://github.com/hampak/python-study/assets/85291626/46210f46-65e8-4ea2-98c5-4b97b02acb49)


## 리스트 데이터 정렬

파이썬에서 리스트, 튜플, 딕셔너리 등에 저장된 데이터를 순서에 의해 정렬해주는 함수가 `sort()`이다. 이 함수는 크게 오름차순과 내림차순이 있며 **리스트변수에 저장된 데이터 항목의 위치를 원하는 순서로 정렬할 수가 있다.**

```py
# 1번 방법
some_list.sort()

# 2번 방법
sorted(some_list)
```

### sort() VS. sorted()

![IMG_08F929966216-1](https://github.com/hampak/python-study/assets/85291626/a82882fe-1314-4c71-b653-264ac5a0f40b)

```py
numList = [43, 12, 3, 7, 72, 25]
numList.sort()
print(numList)

# [3, 7, 12, 25, 43, 72]

numList2 = [9, 12, 1, 6, 3]
print(sorted(numList2)) # [1, 3, 6, 9, 12]
print(numList2) # [9, 12, 1, 6, 3
```

### 내림차순으로 정렬

`reverse = True`를 추가해주면 된다.

```py
num = [15, 11, 9, 6, 3]
num.sort(reverse = True)
print(num)

# [15, 11, 9, 6, 3]

alpha = ["a", "x", "M", "T", "c"]
alpha.sort(reverse = True)
print(alpha)

# ['x', 'c', 'a', 'T', 'M']

alpha1 = ["k", "o", "r", "e", "a"]
print(sorted(alpha1, reverse = True)) # ['r', 'o', 'k', 'e', 'a']
print(alpha1) # ['k', 'o', 'r', 'e', 'a'] --> "sorted"를 사용하면 저장된 내용이 유지되지 않고 원래의 값이 유지됨
```

## 간단한 실습

> 리스트 변수 `numList = [11, 23, 5, 7, 15, 9, 8]`에 숫자 항목이 기억되어 있다. 다음과 같이 출력되도록 하시오.

```
정렬 전: [11, 23, 5, 7, 15, 9, 8]
-----------------
> 정렬 후: [23, 15, 11, 9, 8, 7, 5]
```

```py
numList = [11, 23, 5, 7, 15, 9, 8]

print(f"정렬 전: {numList}")
print("------------------------------")
numList.sort(reverse=True)
print(f"정렬 후: {numList}")

# 정렬 전: [11, 23, 5, 7, 15, 9, 8]
# ------------------------------
# 정렬 후: [23, 15, 11, 9, 8, 7, 5]
