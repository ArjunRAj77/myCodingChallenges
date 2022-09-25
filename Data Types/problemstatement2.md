# Problem Statement
---
- Question Provider : HackerRank
- Question Link: [Nested Lists](https://www.hackerrank.com/challenges/nested-list/problem)

### Description

<img width="857" alt="image" src="https://user-images.githubusercontent.com/23217592/177353301-03c0a492-f789-44cf-ac51-11013c34c12a.png">



### Input Format

<img width="858" alt="image" src="https://user-images.githubusercontent.com/23217592/177353392-1d55f505-5217-4b4e-bd7e-1893be57eac7.png">



# Coding Approach
---
1) Create an empty dictionary.

2) Get the range for number of students.

3) Accepting name of the student from command line.

4) Accepting the grade of the student from command line.

5) Assigning name as key and grade as value for the dictionary.

6) Obtaining the values of dictionary(all grades of students).

7) Removing duplicte grades by using set data type , changing it to list, sorting in ascending order and taking the second lowest grade.

8) Declaring an empty list for storing the name of the students who got the second lowest grade.

9) Going through the name and grade of each students by using items() method of dictionary.

10) Checking whether the grade is equal to the second lowest grade.

11) If yes , append it to the second_lowest list.

12) bSorting the name of students in asceding order

13) Going through the name of each students who got the second lowes grade.

14) Printing each name of students in seperate line.


# Answer

### Programming language used : Python
---
```
if __name__ == '__main__':
    d={} 
    for _ in range(int(input())):
        Name=input() 
        Grade=float(input()) 
        d[Name]=Grade 
    v=d.values()
    second=sorted(list(set(v)))[1] 
    second_lowest=[] 
    for key,value in d.items():  
        if value==second: 
            second_lowest.append(key) 
    second_lowest.sort() 
    for name in second_lowest: 
        print(name)    
    
        

```

