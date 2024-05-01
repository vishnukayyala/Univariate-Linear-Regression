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

# Program to implement univariate Linear Regression to fit a straight line using least squares.
# Developed by: R.KAMESH
# register number: 212223230095

```
import numpy as np 
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)


plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()
```
## Output
![Screenshot 2024-05-01 145711](https://github.com/23002027/Univariate-Linear-Regression/assets/139752981/2ea5db2e-92a3-4d3f-ac00-e49b311c105d)
![Screenshot 2024-05-01 145723](https://github.com/23002027/Univariate-Linear-Regression/assets/139752981/df69eaab-f7d6-4ed5-a0be-e0ade00579c9)
![Screenshot 2024-05-01 145736](https://github.com/23002027/Univariate-Linear-Regression/assets/139752981/8bbeae00-b73d-4a0a-8b4c-092005f7a209)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.







