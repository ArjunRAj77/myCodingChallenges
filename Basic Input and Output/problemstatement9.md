# Problem Statement
---
- Question Provider : HackerRank
- Question Link: [Sequence Equation](https://www.hackerrank.com/challenges/permutation-equation/problem?isFullScreen=true)

### Description

<img width="533" alt="image" src="https://user-images.githubusercontent.com/23217592/177198242-f2e390a6-6eb5-4841-a92a-d6cf2a525278.png">


### Input Format

The first line contains an integer ,n the number of elements in the sequence.
The second line contains  space-separated integers p[i]

<img width="585" alt="image" src="https://user-images.githubusercontent.com/23217592/177198437-edc11561-a4c3-457c-9d54-0e40c6cbc380.png">


# Coding Approach
---
- Create a dictionary with the values of the list p
- traverse through dictinary with the function p[p[x]]

# Answer
---
```
#!/bin/python3

import math
import os
import random
import re
import sys

#
# Complete the 'permutationEquation' function below.
#
# The function is expected to return an INTEGER_ARRAY.
# The function accepts INTEGER_ARRAY p as parameter.
#

def permutationEquation(p):
    dic = {p[i]:i+1 for i in range(len(p))}
    return [dic[dic[i+1]]  for i in range(len(p))]
                        

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    n = int(input().strip())

    p = list(map(int, input().rstrip().split()))

    result = permutationEquation(p)

    fptr.write('\n'.join(map(str, result)))
    fptr.write('\n')

    fptr.close()


```
