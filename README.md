# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
 1. Get the independent variable X and dependent variable Y.
   
 2 . Calculate the mean of the X -values and the mean of the Y -values.
 
 3. Find the slope m of the line of best fit using the formula
 
 4. Compute the y -intercept of the line by using the formula
  
 5 . Use the slope m and the y -intercept to form the equation of the line.

 6. Obtain the straight line
 equation Y=mX+b and plot the scatterplot

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Mohamed Aathil M
RegisterNumber:25008235  
*/
```
 import numpy as np
 import matplotlib.pyplot as plt
 
 x=np.array(eval(input()))
 y=np.array(eval(input()))
 
 x_mean=np.mean(x)
 y_mean=np.mean(y)
  num=0
 denom=0
 
 for i in range(len(x)):
 num+=(x[i]-x_mean)*(y[i]-y_mean)
 denom+=(x[i]-x_mean)**2
 
 m=num/denom
 
 b=y_mean-m*x_mean
 
 print(m,b)
 
 y_predicted=m*x+b
 print(y_predicted)
 
 plt.scatter(x,y)
 plt.plot(x,y_predicted,color='red')
 plt.show()
 
## Output:
<img width="727" height="522" alt="Screenshot 2025-11-11 113223" src="https://github.com/user-attachments/assets/6760b1d0-d945-41a8-ad08-f58cecbe8a27" />



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
