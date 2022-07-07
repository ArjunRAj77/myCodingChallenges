# Problem Statement
---
- Question Provider : HackerRank
- Question Link: [Find the Runner-Up Score!](https://www.hackerrank.com/challenges/find-second-maximum-number-in-a-list/problem)

### Description


<img width="869" alt="image" src="https://user-images.githubusercontent.com/23217592/177365701-f6ca4da8-eb7a-444e-8286-413b23b46917.png">



### Input Format

<img width="868" alt="image" src="https://user-images.githubusercontent.com/23217592/177365732-91ffb5ba-81f2-4f83-9a94-9c23dfeeb799.png">




# Coding Approach
---

- find the maximum number of the list
- remove the maximum number of the list
- display the second largest number


# Answer

### Programming language used : Python3
---
```
if __name__ == '__main__':
    n = int(input())
    arr = list(map(int, input().split()))

    z = max(arr)
    while max(arr) == z:
        arr.remove(max(arr))

    print(max(arr))

```

