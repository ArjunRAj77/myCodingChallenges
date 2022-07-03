# Problem Statement
---
- Question Provider : HackerRank
- Question Link: [Jumping on the clouds problem](https://www.hackerrank.com/challenges/jumping-on-the-clouds/problem)

### Description

There is a new mobile game that starts with consecutively numbered clouds. Some of the clouds are thunderheads and others are cumulus. 
The player can jump on any cumulus cloud having a number that is equal to the number of the current cloud plus 1 or 2.

### Functional Description

Complete the jumpingOnClouds function in the editor below.

jumpingOnClouds has the following parameter(s):

int c[n]: an array of binary integers

### Return 
int: the minimum number of jumps required

### Input Format

The first line contains 26 space-separated integers describing the respective heights of each consecutive lowercase English letter, ascii[a-z].
The second line contains a single word consisting of lowercase English alphabetic letters.

### sampling input
- 7
- 0 0 1 0 0 1 0

### Sampling output

4

# Coding Approach
---
-  everytime a cloud that can be accessed, we are double jumping the cloud, so to check the minimum number of jumps required.

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
# Complete the 'jumpingOnClouds' function below.
#
# The function is expected to return an INTEGER.
# The function accepts INTEGER_ARRAY c as parameter.
#

def jumpingOnClouds(c):
    # Write your code here
    cloudLength=len(c)
    steps=0
    i=0
    while(i<cloudLength-1):
        if c[i] == 0 :
            i+=1
        steps+=1
        i+=1
    return steps
            
            

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    n = int(input().strip())

    c = list(map(int, input().rstrip().split()))

    result = jumpingOnClouds(c)

    fptr.write(str(result) + '\n')

    fptr.close()

```
