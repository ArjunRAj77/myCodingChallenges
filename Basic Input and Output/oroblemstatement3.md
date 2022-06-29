# Problem Statement
---
- Question Provider : HackerRank
- Question Link: [Plus-minus problem](https://www.hackerrank.com/challenges/a-very-big-sum/problem?isFullScreen=true)
<p>
  
Given an array of integers, calculate the ratios of its elements that are positive, negative, and zero. Print the decimal value of each fraction on a new line with  places after the decimal.

Note: This challenge introduces precision problems. The test cases are scaled to six decimal places, though answers with absolute error of up to  are acceptable.

### Example

There are  elements, two positive, two negative and one zero. Their ratios are ,  and . Results are printed as:

0.400000
0.400000
0.200000

### Function Description

Complete the plusMinus function in the editor below.

plusMinus has the following parameter(s):

int arr[n]: an array of integers
Print
Print the ratios of positive, negative and zero values in the array. Each value should be printed on a separate line with  digits after the decimal. The function should not return a value.
.</p>

### Input Format

The first line contains an integer, n, the size of the array.
The second line contains  space-separated integers that describe array[n].

### Output Format

Print the following 3 lines, each to 6 decimals:

1. proportion of positive values
2. proportion of negative values
3. proportion of zeros


# Coding Approach
---
- get the number of positive, negative and zeroes in the array
- find out the ration of the above numbers with total number of elements in the array
- print the ratio with upto 6 decimals

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
# Complete the 'plusMinus' function below.
#
# The function accepts INTEGER_ARRAY arr as parameter.
#

def plusMinus(arr):
    # Write your code here
    arrLength=len(arr)
    postive=0
    negative=0
    zero=0
    for i in arr:
        if i >0 :
            postive+=1
        elif i<0:
            negative+=1
        else:
            zero+=1
    posRatio=format(postive/arrLength,'.6f')
    negRatio=format(negative/arrLength,'.6f')
    zeroRatio=format(zero/arrLength,'.6f')
    print(posRatio)
    print(negRatio)
    print(zeroRatio)

if __name__ == '__main__':
    n = int(input().strip())

    arr = list(map(int, input().rstrip().split()))

    plusMinus(arr)


```
