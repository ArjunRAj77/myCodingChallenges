# Problem Statement
---
- Question Provider : HackerRank
- Question Link: [Stair case problem](https://www.hackerrank.com/challenges/staircase/problem?isFullScreen=true&h_r=next-challenge&h_v=zen)

### Description
ts base and height are both equal to n. It is drawn using # symbols and spaces. The last line is not preceded by any spaces.

Write a program that prints a staircase of size n.


```
     #
    ##
   ###
  ####
 #####
######

```

### Input Format

A single integer,n , denoting the size of the staircase.

### Output Format
the staircase of size n



# Coding Approach
---
- print the '#' and ' ' in an oppsite way

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
# Complete the 'staircase' function below.
#
# The function accepts INTEGER n as parameter.
#

def staircase(n):
    # Write your code here
    temp=n-2
    for i in range(1,n):
        print (" " * temp,"#" * i)
        temp -= 1
    print("#"*n)   

if __name__ == '__main__':
    n = int(input().strip())

    staircase(n)


```
