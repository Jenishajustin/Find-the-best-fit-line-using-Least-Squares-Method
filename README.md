# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: J JENISHA
RegisterNumber:  212222230056
```

```python
import numpy as np
x=np.array(eval(input()))
y=np.array(eval(input()))

x_mean=np.mean(x)
y_mean=np.mean(y)

num=0
den=0

for i in range(len(x)):
    num+=(x[i]-x_mean)*(y[i]-y_mean)
    den+=(x[i]-x_mean)**2

m=num/den
c=y_mean-m*x_mean

print('Slope:',m)
print('Y-intercept:',c)

y_prediction=m*x+c
print('Predicted values:\n',y_prediction)

import matplotlib.pyplot as plt
plt.scatter(x,y)

plt.plot(x,y_prediction,color='purple')
plt.show()
```

## Output:

![Screenshot from 2024-02-22 10-22-47](https://github.com/Jenishajustin/Find-the-best-fit-line-using-Least-Squares-Method/assets/119405070/f2f4ef64-cc3f-4e72-ab15-213c6304661d)
<br>

![Screenshot from 2024-02-22 10-23-01](https://github.com/Jenishajustin/Find-the-best-fit-line-using-Least-Squares-Method/assets/119405070/d08998e1-d2d2-4b75-ace8-24fa37e8f5f5)
<br>

#### Best Fit Line
![Screenshot from 2024-02-22 10-23-34](https://github.com/Jenishajustin/Find-the-best-fit-line-using-Least-Squares-Method/assets/119405070/6a4c9700-c983-4b5e-b306-ca6cff3b233d)
<br>

![Screenshot from 2024-02-22 10-23-46](https://github.com/Jenishajustin/Find-the-best-fit-line-using-Least-Squares-Method/assets/119405070/57f214ea-1f96-4d0c-9a4c-f4b7e1036a43)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
