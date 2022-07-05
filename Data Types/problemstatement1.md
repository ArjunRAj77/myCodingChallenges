# Problem Statement
---
- Question Provider : HackerRank
- Question Link: [List Comprehensions](https://www.hackerrank.com/challenges/list-comprehensions/problem)

### Description

<img width="863" alt="image" src="https://user-images.githubusercontent.com/23217592/177323770-10393bf3-b596-4a8d-b691-2a0950a0c58e.png">


### Input Format

<img width="862" alt="image" src="https://user-images.githubusercontent.com/23217592/177323879-70fd6bc0-a158-4aa4-9483-b7dff67f140a.png">


# Coding Approach
---
- create a list of permutations and collect the sum of each list
- check the sum of each list with the condition.


# Answer

### Programming language used : Python
---
```
if __name__ == '__main__':
    x = int(input())
    y = int(input())
    z = int(input())
    n = int(input())
    print ([[a,b,c] for a in range(0,x+1) for b in range(0,y+1) for c in range(0,z+1) if a + b + c != n ])


```

