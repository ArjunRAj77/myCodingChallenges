# Problem Statement
---
- Question Provider : HackerRank
- Question Link: [Angry Proffessor](https://www.hackerrank.com/challenges/angry-professor/problem?isFullScreen=true)

### Description

A Discrete Mathematics professor has a class of students. 
Frustrated with their lack of discipline, the professor decides to cancel class if fewer than some number of students are present when class starts.

### Functional Description

Complete the angryProfessor function in the editor below. It must return YES if class is cancelled, or NO otherwise.

angryProfessor has the following parameter(s):

- int k: the threshold number of students
- int a[n]: the arrival times of the  students

### Return 
- string: either YES or NO

### Input Format

The first line contains 26 space-separated integers describing the respective heights of each consecutive lowercase English letter, ascii[a-z].
The second line contains a single word consisting of lowercase English alphabetic letters.

### sampling input
- 2
- 4 3
- -1 -3 4 2
- 4 2
- 0 -1 2 1

### Sampling output

- YES
- NO
# Coding Approach
---
-  Count the number of students arriving on time
-  check the count value satifies the thresh hold and display appropriate message.

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
# Complete the 'angryProfessor' function below.
#
# The function is expected to return a STRING.
# The function accepts following parameters:
#  1. INTEGER k
#  2. INTEGER_ARRAY a
#

def angryProfessor(k, a):
    # Write your code here
    n=len(a)
    checker=0
    for student in a:
        if student <=0 :
            checker+=1       
    if checker <k:
        return "YES"
    else :
        return "NO"        
            

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    t = int(input().strip())

    for t_itr in range(t):
        first_multiple_input = input().rstrip().split()

        n = int(first_multiple_input[0])

        k = int(first_multiple_input[1])

        a = list(map(int, input().rstrip().split()))

        result = angryProfessor(k, a)

        fptr.write(result + '\n')

    fptr.close()


```
