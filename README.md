# Implementation of Univariate Linear Regression


## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
Step 1. Start
Step 2. Get the independent variable X and dependent variable Y.
Step 3. Calculate the mean of the X -values and the mean of the Y -values.
Step 4. Find the slope m of the line of best fit using the formula. 
Step 5. Compute the y -intercept of the line by using the formula:
Step 6. Use the slope m and the y -intercept to form the equation of the line.
Step 7. End
```
## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Iswarya P
RegisterNumber: 212223230082 
*/

import numpy as np
import matplotlib.pyplot as plt
X=np.array(eval(input("Enter X value:")))
Y=np.array(eval(input("Enter Y value:")))
X_mean=np.mean(X)
Y_mean=np.mean(Y)
num=0
denom=0
for i in range(len(X)):
    num+=(X[i]-X_mean)*(Y[i]-Y_mean)
    denom+=(X[i]-X_mean)**2
m=num/denom
b=Y_mean-m*X_mean
print("The m value is: ",m)
print("The b value is: ",b)
y_predicted=m*X+b
print("The Y_Predicted value is: ",y_predicted)
plt.scatter(X,Y)
plt.plot(X,y_predicted,color='red')
plt.show()
```

## Output:

![image](https://github.com/user-attachments/assets/73118cbd-f4eb-4f71-ab9b-fe13b22ecdea)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
