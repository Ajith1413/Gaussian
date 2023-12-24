# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
## Step:1. 
Import the numpy module to use the built-in functions for calculation.
## Step:2. 
Import the sys module to use the built-in funtions.
## Step:3. 
Get input from the user for number of rows and add it by 1 for number of columns.
## Step:4. 
Using np.zeros() set the matrix as null matrix.
## Step:5.
Using for loop get input from the user for each element in the matrix.
## Step:6.
Using for loop we can perform the elementary row operations and find the final matrix.
## Step:7.
Print the values by solving the matrix using for loop with 2 point precision.
## Step:8.
End the program.
## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.

'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: AJITH KUMAR A
RegisterNumber: 23002150
'''
import numpy as np
n=int(input())
arr=np.zeros((n,n+1))
res=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        arr[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=arr[j][i]/arr[i][i]
        for k in range(n+1):
            arr[j][k]=arr[j][k]-ratio*arr[i][k]
res[n-1]=arr[n-1][n]/arr[n-1][n-1]
for i in range(n-1,-1,-1):
    res[i]=arr[i][n]
    for j in range(i+1,n):
        res[i]=res[i]-arr[i][j]*res[j]
    res[i]=res[i]/arr[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,res[i]), end=" ")
 
*/
```

## Output:
![Alt text](image.png)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

