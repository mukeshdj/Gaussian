# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. import numpy module and sys module
2. Get input from the user for number of rows and add it by 1 for number of column
3. Using np.zeros() set the matrix as null matrix.
4. Using nested for loop find the ratio and perform the elementary row operations and find the final matrix.
5. Print and end the program
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
a[ j] [k]=a[j][k]-ratio*a[i̱][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):

for j in range(i+1,n):
x[i]=x[i]-a[i][j]*x[j]
x[i]=x[i]/a[i][i]
for i in range(n):
print('X%d=%0.2f' %(i,x[i]),end=' ')
## Output:
![image](https://github.com/AkilaMohan/Gaussian/assets/155506353/2be92fce-4ca9-4364-be22-392c65c88088)
![image](https://github.com/AkilaMohan/Gaussian/assets/155506353/e2e8999c-cced-45cb-9d80-f896c69852ae)




## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

