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
SWETHA A
212223220114
```
```

import numpy as np
import matplotlib.pyplot as plt
x = np.array(eval(input()))
y = np.array(eval(input()))
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

plt.scatter(x,y,color='Black')
plt.plot(x,ypred,color='pink')
plt.show()

```
## Output:
![Screenshot 2025-03-01 190834](https://github.com/user-attachments/assets/0c50b3e4-87a0-4df0-8eda-92525b22d383)

![Screenshot 2025-03-01 190845](https://github.com/user-attachments/assets/90e88171-893a-4028-a986-d89a5cecc8e9)


![Screenshot 2025-03-01 190854](https://github.com/user-attachments/assets/100d24d2-52ba-4f21-b6b2-087c81721f1b)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
