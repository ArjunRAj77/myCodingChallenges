# Problem Statement
---
- Question Provider : HackerRank
- Question Link: [Design PDF Viewer problem](https://www.hackerrank.com/challenges/designer-pdf-viewer/problem?isFullScreen=true)

### Description
When a contiguous block of text is selected in a PDF viewer, the selection is highlighted with a blue rectangle. 
In this PDF viewer, each word is highlighted independently.

### Functional Description

Complete the designerPdfViewer function in the editor below.

designerPdfViewer has the following parameter(s):

int h[26]: the heights of each letter
string word: a string

### Input Format

The first line contains 26 space-separated integers describing the respective heights of each consecutive lowercase English letter, ascii[a-z].
The second line contains a single word consisting of lowercase English alphabetic letters.


# Coding Approach
---
- get the order number of the character from the string 
- compare the order number with 97
- get the corresponding indexing height
- find out the maximum value in newly created height array
- find the area by multiplying the max height with length of the string

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
# Complete the 'designerPdfViewer' function below.
#
# The function is expected to return an INTEGER.
# The function accepts following parameters:
#  1. INTEGER_ARRAY h
#  2. STRING word
#

def designerPdfViewer(h, word):
    # Write your code here
    width=len(word)
    height=[]
    for s in word:
        ordervalue=ord(s)-97
        data=h[ordervalue]
        height.append(data)
    length=max(height)
    area=length*width
    return area
        

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    h = list(map(int, input().rstrip().split()))

    word = input()

    result = designerPdfViewer(h, word)

    fptr.write(str(result) + '\n')

    fptr.close()


```
