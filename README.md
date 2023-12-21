# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import numpy library as np.
2. Create a matrix.
3.Get the output and end the program.
## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: GOKHULRAJ V
RegisterNumber: 23004889
*/
```
```
import numpy as np
import sys
n=int(input())
matrix=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        matrix[i][j]=int(input())
for i in range(n):
    if matrix[i][i]==0.0:
        sys.exit("Divide by zero error")
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
```
## Output:

![Screenshot 2023-12-21 185513](https://github.com/Gokhulraj2005/Gaussian/assets/138849253/d25f1e02-c3b0-4123-a584-3b765436ac20)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

