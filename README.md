# SWE_2021_41_2024_2_week_6
---
## Week 4 Assignment
* Link of repository
>https://github.com/kwonseungho0514/SWE_2021_41_2024_2_week_4
* Code
>```Python
>history = []
>
>def isHappy(n):
>  if (n < 1 or n > pow(2,31) - 1):
>    return False
>
>  while(in_history(n) != True):
>    history.append(n)
>    n = next_n(n)
>
>  if (n == 1):
>    return True
>  else:
>    return False
>
>def in_history(n):
>  for i in range(len(history)):
>    if (n == history[i]):
>      return True
>  return False
>def next_n(n):
>  nums = []
>  sum = 0
>
>  while(n != 0):
>    nums.append(n % 10)
>    n= n // 10
>  for i in range(len(nums)):
>    sum += nums[i] * nums[i]
>  return sum
>
>num = (int)(input())
>print(isHappy(num))
>```

* Description of code
 먼저 입력된 n이 범위에서 벗어난 값인지 확인한다. 만약 범위 내의 값이라면 n이 Happy Number인지 확인한다.
 1단계로 in_history 함수를 이용하여 지금 입력된 n이 이전에 입력되어서 루프를 돌고 있는 것인지 확인한다. 이전에 입력되었는지의 유무를 확인하기 위해 history라는 array를 두어 만약 입력된 적 없는 n이라면 history에 추가하여 기록되도록하였다.
 2단계로 
---
## Week 5 Assignment

> ```Shell
> docker exec ossp-container cat /etc/os-release
> ```
> ossp-container에 접속하여 현재 os의 이름과 버전을 확인할 수 있는 commandline이다.이에 따른 실행결과는 다음과 같으며 이름은 "Ubuntu"이고 버전은 "24.04.1 LTS (Noble Numbat)"임을 알 수 있다.

> ```Shell
> docker exec ossp-container git --version
> ```
> ossp-container에 접속하여 현재 설치된 git의 버전을 확인할 수 있는 commandline이다. 이에 따른 실행결과는 다음과 같으며 2.43.0 버전임을 알 수 있다.

> ```Shell
> docker exec ossp-container python3 --version
> ```
> ossp-container에 접속하여 현재 설치된 python3의 버전을 확인할 수 있는 commandline이다. 이에 따른 실행결과는 다음과 같으며 3.12.3 버전임을 알 수 있다.

> ```Shell
> docker inspect --format="{{.HostConfig.Binds}}" ossp-container
> ```
> ossp-container의 세부 정보중 mount directory를 확인할 수 있는 commandline이다. 이에따른 실행결과는 다음과 같으며 [C:\Users\Seungho\ossp_host_dir:/mnt/ossp_container_dir]임을 알 수 있다.
