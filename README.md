# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Input
2. Forward Elimination (Convert matrix to Upper Triangular Form)
3. Back Substitution (Solve the upper triangular matrix)
4. Output

## Program:
```

Program to find the solution of a matrix using Gaussian Elimination.
Developed by: MAHA VISHNU S
RegisterNumber: 25018250



import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0.0:
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
    print('X%d = %0.2f' %(i,x[i]),end=' ')


```

## Output:
<img width="1215" height="625" alt="MA EXP 6 QUES" src="https://github.com/user-attachments/assets/53839bad-c334-406b-9854-5afe1fabe2d7" />
<img width="1180" height="772" alt="MA EXP 6 ANS" src="https://github.com/user-attachments/assets/e07942dc-7ea8-47a3-926d-83720810e165" />
<img width="1247" height="682" alt="MA EXP 6 ANS SEC" src="https://github.com/user-attachments/assets/0703ca76-04a7-483e-b107-808f330c4968" />





## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

