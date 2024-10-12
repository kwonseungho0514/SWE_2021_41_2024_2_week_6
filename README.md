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
'''
* Description of code
  
---
## Week 5 Assignment

> ```Shell
> docker exec ossp-container cat /etc/os-release
> ```
> ```Shell
> docker exec ossp-container git --version
> ```
> ```Shell
> docker exec ossp-container python3 --version
> ```
> ```Shell
> docker inspect --format="{{.HostConfig.Binds}}" ossp-container
> ```
