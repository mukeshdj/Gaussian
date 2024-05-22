# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.First,we want to import numpy,then import sys,assume a variable.
2. For gaussian elimination method, we want to make 2nd and 3rd column zero.
3. For that we want to make a range accorting to our program output.
4. Then print the program with correct form then the output will display.
   

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: MUKESH S
RegisterNumber: 2305002016
*/
```
````
import numpy as np
n=int(input())
matrix=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        matrix[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=matrix[j][i]/matrix[i][i]
        for k in range(n+1):
            matrix[j][k]=matrix[j][k]-ratio*matrix[i][k]
x[n-1]=matrix[n-1][n]/matrix[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=matrix[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-matrix[i][j]*x[j]
    x[i]=x[i]/matrix[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=" ")
````


## Output:
![gaussian elimination]()
![Screenshot 2024-05-22 214405](https://github.com/AkilaMohan/Gaussian/assets/155506353/2d534a73-c9ec-4247-8a11-6727b76cd979)
![image](https://github.com/AkilaMohan/Gaussian/assets/155506353/ec99f581-ff14-481a-ad46-c2cfcdfb0be8)






## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

