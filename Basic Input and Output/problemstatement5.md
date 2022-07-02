# Problem Statement
---
- Question Provider : HackerRank
- Question Link: [Counting alleys problem](https://www.hackerrank.com/challenges/counting-valleys/problem?isFullScreen=true)

### Description
An avid hiker keeps meticulous records of their hikes. During the last hike that took exactly _Steps_ steps, for every step it was noted if it was an uphill, **U** , or a downhill, **D** step. Hikes always start and end at sea level, and each step up or down represents a  unit change in altitude. We define the following terms:

A mountain is a sequence of consecutive steps above sea level, starting with a step up from sea level and ending with a step down to sea level.
A valley is a sequence of consecutive steps below sea level, starting with a step down from sea level and ending with a step up to sea level.
Given the sequence of up and down steps during a hike, find and print the number of valleys walked through.

### Example

 - steps = 8 
 - path =[DDUUUUUDD]

The hiker first enters a valley 2 units deep. Then they climb out and up onto a mountain 2 units high. 
Finally, the hiker returns to sea level and ends the hike.

### Function Description

Complete the countingValleys function in the editor below.

countingValleys has the following parameter(s):

- int steps: the number of steps on the hike
- string path: a string describing the path


# Coding Approach
---
- figure out number of time you came back up to the sea level

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
# Complete the 'countingValleys' function below.
#
# The function is expected to return an INTEGER.
# The function accepts following parameters:
#  1. INTEGER steps
#  2. STRING path
#

def countingValleys(steps, path):
    # Write your code here
    level=0
    valley=0
    for value in path:
        if value =='U':
            level+=1
        if value == 'D':
            level-=1
        if level==0 and value == 'U':
            valley+=1
    return valley 
if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    steps = int(input().strip())

    path = input()

    result = countingValleys(steps, path)

    fptr.write(str(result) + '\n')

    fptr.close()

```
