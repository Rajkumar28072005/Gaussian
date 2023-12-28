# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Start the program.
2. import numpy,import sys.
3. Use gaussian solving methods.
4. Display the values.

## Program:
```
Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Dhandeeswaran selvakumar
RegisterNumber: 23006838
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
        for k in range (n+1):
            arr[j][k]=arr[j][k]-ratio*arr[i][k]
res[n-1]=arr[n-1][n]/arr[n-1][n-1]
for i in range(n-2,-1,-1):
    res[i]=arr[i][n]
    for j in range(i+1,n):
        res[i]=res[i]-arr[i][j]*res[j]
    res[i]=res[i]/arr[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,res[i]),end=" ") 
```

## Output:
![Screenshot 2023-12-28 221321](https://github.com/dhandeeswaran2005/Gaussian/assets/147139188/468f8fb9-a81c-4e36-9128-3dab8fcdbd60)





## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

