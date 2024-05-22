# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import numpy library using import statement.

2. Import sys library

3. Create a variable n to recieve to recieve dimention of the matrix.

4. using input n,create a zero matrix 'a' of nx(n+1) and a zero row matrix 'x' of n using np.zeros().

5. Initiate 1st nested for loop to get values from user and store it in the 'a' matrix using float(input()).

6. Initiate 2nd nested for loop to apply gaussian elimination.

7. Initiate 3rd nested for loop to calculate the solution of the 'a' matrix using back substitution.

8. Display the solution for each variable upto 2 decimals using for loop and print() with '%' operator.
## Program:
```
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: MUKESH S
RegisterNumber: 2305002016
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
![Screenshot 2024-05-22 214405](https://github.com/AkilaMohan/Gaussian/assets/155506353/fe04f524-396e-4d52-82de-e1c2def7eb8b)
![image](https://github.com/AkilaMohan/Gaussian/assets/155506353/7fc00bf8-55f7-4d38-8346-8609dcce55f5)

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

