## 중첩반복문

중첩반복문은 외부 `for`반복문 내에 **또 다른** 내부 `for`반복문을 내포하고 있는 구조이다. **외부 반복문이 1회 수행할 때마다 내부 반복문 전체가 수행된다.**

```py
for i in range():
  # executed code
  for y in range():
    # executed code
```

이것을 간단한 예제로 살펴보자:

```py
for i in range(2):
  print("i = ", i)
  for j in range(3):
    print("\tj = ", j)

# i =  0
#        j =  0
#        j =  1
#        j =  2
# i =  1
#        j =  0
#        j =  1
#        j =  2
```

