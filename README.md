# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
![image](https://github.com/mukeshdj/Gaussian/assets/155506353/7cfbc104-66b4-42f9-a8ac-5571bd764678)

## Program:
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: MUKESH S
RegisterNumber: 2305002016
*/
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
for j in range(n+1):
a[i][j]=float(input())
for i in range(n):
if a[i][i] == 0.0:
sys.exit("Divide by zero detected!")
for j in range(i+1,n):
ratio=a[j][i]/a[i][i]
for k in range(n+1):
a[ j] [k]=a[j] [k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
x[i]=a[i][n]
for j in range(i+1,n):
x[i]=x[i]-a[i][j]*x[j]
x[i]=x[i]/a[i][i]
for i in range(n):
print('X%d =%0.2f' %(i,x[i]),end=' ')

## Output:
![image](https://github.com/mukeshdj/Gaussian/assets/155506353/3d61226f-a7d0-4dbe-8e43-9c568a108cb6)
![image](https://github.com/mukeshdj/Gaussian/assets/155506353/3cfa322b-5c16-4b7d-b590-1ab95f6a6701)




## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

