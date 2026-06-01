# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Read the number of variables, augmented matrix coefficients, and initialize solution arrays.
2.Apply Gaussian Elimination to convert the matrix into upper triangular form while checking for divide-by-zero errors.
3.Use Back Substitution to calculate the values of unknown variables starting from the last equation.
4.Print the computed values of all variables in the system of equations. 

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: vijayaprathisha J
RegisterNumber:212225240184
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
        
for i in range(n):
    if a[i][j]==0.0:
        sys.exit('Divide by zero detected!')
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        
        for k in range(n+1):
            a[j][k]=a[j][k]- ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
    
for i in range(n):
    print('X%d = %0.2f' %(i,x[i]),end=' ')
*/
```

## Output:

<img width="1450" height="1959" alt="image" src="https://github.com/user-attachments/assets/e9c97224-c0e3-466b-917c-4cbe8c45144f" />

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

