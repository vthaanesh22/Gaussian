# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import the numpy module and sys module to use the built-in functions for calculation
2. Get the size of the matrix from user and create empty matrix and vector
3. using for loop get elements for matrix and vector
4. Using another for loop to take each element in the matrix
5. solve row echelon form
6. perform back substitution
7. print the value in two decimal points
8. End the program 
 

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by:V.Thaanesh 
RegisterNumber: 23003843
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
        
for i in range(n):
    if a[i][i]==0:
        sys.exit("Divide by zero detected!")
        
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
            
x[n-1]=a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    
    x[i]=x[i]/a[i][i]
    
for i in range(n):
    print("X%d = %0.2f"%(i,x[i]),end=" ")

*/
```

## Output:
![output](/Screenshot%202023-07-27%20113126.png)

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

