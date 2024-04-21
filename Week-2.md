파이썬에서는 `>>>` 모양을 프롬트라고 하며, 이 상태에서 간단한 프로그램을 작성할 수 있는 상태를 쉘 모드라고 한다.

쉘 모드에서 조금 더 긴 코드를 작성하고 싶다면, 혹은 메모장과 비슷한 텍스트 에디터를 이용하여 소스 코드를 파일에 저장하며 실행하고 열고 싶다면 **script mode**를 이용하면 된다.

## print() 함수

간단한 문자열을 출력하기 위해서는 `print()` 함수를 사용한다.

```py
print("I kinda love javascript")
```

프린트 함수 내에서 간단한 연산식을 계산할 수도 있다

```py
print(10 + 10)
# 20
```

문자열과 연산식을 같이 사용할 수 있는데, 이것은 쉼표(,)를 응용하여 가능케 한다. 예를 들어,

```py
print("10 + 10 =", 10 + 10)
# 10 + 10 = 20
```

> 여기서 주의해야할 점은 쉼표를 사용하면 스페이스(공백)이 하나 생긴다.

두 개 이상의 문자열을 `+` 연산자와 `,`를 사용하여 합칠 수 있다. 예를 들어,

```py
print("python"+"program")
# pythonprogram

print("python","program")
# python program
```

`*` 연사자를 활용하여 문자열을 제시된 수만큼 "곱"할 수 있다.

```py
print("Javascript " * 5)
# Javascript Javascript Javascript Javascript Javascript
# Javascript 오른쪽에 공백을 하나 넣었기 때문에 출력문에도 공백이 존재한다.
```

![IMG_8531D6D0065D-1](https://github.com/hampak/python-study/assets/85291626/5b28ad65-bab8-4744-984b-e042c1e43adb)

왼쪽에 있는 것이 스크립트 모드, 오른쪽에 있는 것이 쉘 모드이다.
