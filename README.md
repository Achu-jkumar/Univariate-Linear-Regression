# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
~~~
Name:J.Archana priya 
Ref.no:21500533
~~~
```
import numpy as np
import matplotlib.pyplot as plt
x=np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
y=np.array([1, 3, 2, 5, 7, 8, 8, 9, 10, 12])    
plt.scatter(x,y)
plt.show()
x_mean=np.mean(x)
y_mean=np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-x_mean)*(y[i]-y_mean)
    den+=(x[i]-x_mean)**2
m=num/den
b=y_mean-m*x_mean
print(m,b)


y_pred=m*x + b
print(y_pred)

plt.scatter(x,y)
plt.plot(x,y_pred,color='red')
plt.show()
```

## Output:
![ex09](./ex09.png)

## Result:
The univariate Linear Regression to fit a straight line using least squares has been successfully implemented.

