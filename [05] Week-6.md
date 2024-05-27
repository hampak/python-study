## if 조건문

if 조건문은 주어진 조건이 **참일 때만** 해당하는 문을 실행하고 거짓이면 아무것도 실행하지 않는다.

```
if 조건식:
  처리할 문
```

예를 들어,

```py
num = int(input("숫자 입력: "))

if num < 10:
  print("10보다 작은 숫자입니다.")

# 숫자 입력: 8
# 10보다 작은 숫자입니다.
```

또한, 조건 문 내에 있는 문의 indenting이 같다면, 같이 실행된다. 예를 들어,

```py
num = int(input("숫자 입력: "))

if num < 10:
  print("10보다 작은 숫자입니다.")
  print("프로그램을 종료합니다.")
print("10보다 큰 숫자입니다.") # if문이 거짓이면 조건문 내에 아무것도 실행되지 않으며 바로 다음 코드로 넘어간다.

# 숫자 입력: 6
# 10보다 작은 숫자입니다.
# 프로그램을 종료합니다.
# 10보다 큰 숫자입니다.

# 숫자 입력: 11
# 10보다 큰 숫자입니다.
```

## if ~ else 조건문

참인 경우 `if`문에 해당되는 것을 실행하며, 거짓인 경우 `else`에 해당되는 코드를 실행한다.

```py
num = int(input("숫자 입력: "))

if num < 10:
  print("10보다 작은 숫자입니다.")
else:
  print("10보다 큰 숫자입니다.")

# 숫자 입력: 16
# 10보다 큰 숫자입니다.
```

## 간단한 연습

> 컴퓨터 기사 시험 점수 5괴목(소프트웨어설계, 소프트웨어개발,데이터베이스구축,프로그래밍언어 활용, 정보시스템 구축관리) 점수를 입력하여 과목 40점이상, 전과목 평균 60점이상이면 “합격＂을 출력하고 그렇지 않으면 “불합격＂을 출력하는 프로그램을 작성하시오.

```py
test1 = int(input("소프트웨어 설계: "))
test2 = int(input("소프트웨어 개발: "))
test3 = int(input("데이터베이스 구축: "))
test4 = int(input("프로그래밍언어 활용: "))
test5 = int(input("정보시스템 구축관리: "))

average = (test1 + test2 + test3 + test4 + test5) // 5

print(average)

if (test1 >= 40 and test2 >= 40 and test3 >= 40 and test4 >= 40 and test5 >= 40) and average >= 60:
  print("합격")
else:
  print("불합격")

# 소프트웨어 설계: 70
# 소프트웨어 개발: 60
# 데이터베이스 구축: 80
# 프로그래밍언어 활용: 90
# 정보시스템 구축관리: 40
# 68
# 합격
```

> 사용자로부터 학점을 입력 받아 4.0이상이면 “장학금 신청 대상＂이고 그렇지 않으면 “장학금 학점 미달”을 출력하는 프로그램을 작성하시오.

```py
gpa = float(input("학점 입력: "))

if(gpa >= 4.0):
  print("장학금 신청 대상")
else:
  print("장학금 학점 미달")

# 학점 입력: 4.3
# 장학금 신청 대상
```

> 사용자로부터 어떤 숫자를 입력 받아 홀수인지 짝수인지를 판별하는 프로그램을 작성하시오.

```py
num = int(input("숫자를 입력하시오: "))

if (num % 2 == 0):
  print(f"입력한 숫자 {num}은/는 짝수이다.")
else:
  print("입력한 숫자 {0}은/는 홀수이다".format(num))

# 숫자를 입력하시오: 2
# 입력한 숫자 2은/는 짝수이다.
```

---

## 중첩 if 문

`if`문 내에 또 `if`문을 사용할 수 있다.

예를 들어...

> 사용자로부터 나이를 입력받아 나이가 14세 미만인 경우, “초등학생”, 14세 이상 20세 미만인 경우 “중고등학생”, 나이가 20세 이상인 경우 “대학생”으로 출력하라

```py
age = int(input("나이를 입력하시오: "))

if age >= 14:
  if age < 20:
    print("중고등학생")
  else:
    print("대학생")
else:
  print("초등학생")

# 나이를 입력하시오: 24
# 대학생
```

> 사용자로부터 어떤 정수 하나를 입력 받아 50보다 크고 100보다 작은 경우, 100보다 큰 경우, 50보다 작은 경우의 조건을 중첩if 명령을 이용하여 출력 결과와 같이 출력되도록 프로그램을 작성하시오

```py
num = int(input("숫자를 입력하시오: "))

if num >= 50:
  if num <= 100:
    print(f"입력한 수 {num}은/는 50보다 크고 100보다 작습니다.")
  else:
    print("입력한 수 {0}은/는 100보다 큰 수입니다.".format(num))
else:
  print(f"입력한 수 {num}은/는 50보다 작습니다.")

# 숫자를 입력하시오: 12
# 입력한 수 12은/는 50보다 작습니다.
```

## if ~ elif ~ else 문

`if ~ elif ~ else`문은 가독성을 높이면서 조건문을 조금 더 유용하게 해준다. **`elif`에는 `if`와 똑같이 조건식을 필요로 한다**.

> 숫자 정수 하나를 입력받아 양수인지, 제로(0)인지, 음수인지를 판별하는 중첩 if문

```py
num = int(input("수를 입력하시오: "))

if num == 0:
  print("0")
elif num > 0:
  print("positive number")
else:
  print("negative number")

# 수를 입력하시오: -124124
# negative number
```

## 간단한 연습

> 사용자로부터 어떤 정수 하나를 입력받아 숫자에 따라 한 자릿수, 두 자릿수, 세 자릿수, 네 자릿수를 출력하는 프로그램을 작성하시오.

```py
num = int(input("수를 입력하시오: "))

if num >= 1000:
  print(f"입력한 {num}은/는 네 자릿수 입니다.")
elif num >= 100:
  print(f"입력한 {num}은/는 세 자릿수 입니다.")
elif num >= 10:
  print(f"입력한 {num}은/는 두 자릿수 입니다.")
else:
  print("입력한 수 {0}은/는 한 자릿수 입니다.".format(num))

# 수를 입력하시오: 124   
# 입력한 124은/는 세 자릿수 입니다.
```