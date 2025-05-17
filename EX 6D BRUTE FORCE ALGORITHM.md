# EX 6D BRUTE FORCE ALGORITHM
## DATE:
## AIM:
To write a python program using brute force method of searching for the given substring in the main string.




## Algorithm
1.Generate all possible permutations of the input elements. 
2.Initialize a variable to keep track of the best (optimal) solution found so far. 
3.Fr each permutation, calculate the cost or value of that arrangement. 
4.Cmpare the calculated cost with the best solution and update if better. 
5.After checking all permutations, return the best solution found. 

## Program:
~~~
To implement the program using brute force method of searching for the given substring in the main string.


Developed by: RAKSHITHA K
Register Number:  212223230009

import re #Import this package
def match(str1,str2):
    ########### Add your code here #######
    #Start here
    pattern = re.compile(str2)
    r = pattern.search(str1)
    while r:
        print("Found at index {}".format(r.start()))
        r = pattern.search(str1,r.start() + 1)
    #End here
str1=input()
str2=input()
~~~

## Output:
![image](https://github.com/user-attachments/assets/cbbafb0c-cdb0-4065-8b83-782868f13985)

## Result:
Thus the above program was executed successfully for searching the substring at respective index.
