# Problem Statement
---
- Question Provider : HackerEarth
- Question Link: [Ali and Helping innocent people](https://www.hackerearth.com/practice/basic-programming/input-output/basics-of-input-output/practice-problems/algorithm/cartag-948c2b02/)

<p>Arpasland has surrounded by attackers. 
  A truck enters the city. The driver claims the load is food and medicine from Iranians. 
  Ali is one of the soldiers in Arpasland. He doubts about the truck, maybe it's from the siege. 
  </p>He knows that a tag is valid if the sum of every two consecutive digits of it is even and its letter is not a vowel. Determine if the tag of the truck is valid or not.
<p>
We consider the letters "A","E","I","O","U","Y" to be vowels for this problem.
</p>

### Input Format

The first line contains a string of length 9. The format is "DDXDDD-DD", where D stands for a digit (non zero) and X is an uppercase english letter.

### Output Format

Print "valid" (without quotes) if the tag is valid, print "invalid" otherwise (without quotes)

- Sample Input : 12X345-67
- Sample Output : invalid


# Coding Approach
---
- check the vowels are present in third position of the input
- check the sum of consecutive digits are even
- flag varaible is triggered if condition is failed
- print corresponding response

# Answer

### Programming language used : Python
---
```
Tag=input()#DDXDDD-DD format
vowels=["A","E","I","O","U","Y"]
#valid if sum of every consecutive digitss is even
#valid if letter is not a vowel
sum1=int(Tag[0]+Tag[1])   
sum2=int(Tag[3]+Tag[4])
sum3=int(Tag[4]+Tag[5])
sum4=int(Tag[7]+Tag[8])
flag=False
if ((sum1%2!=0) or (sum2%2!=0) or (sum3%2!=0) or (sum4%2!=0)):
    flag=True
else:
    flag=False
if Tag[3] in vowels:
    flag=True
if(flag==True):
    print("invalid")
else:
    print("valid")
```
