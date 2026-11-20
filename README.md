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
```

import numpy as np
import matplotlib.pyplot as plt
X=np.array([2, 3, 5, 7, 9])
Y=np.array([4, 5, 7, 10, 15] )
num=0
deno=0
X_mean=np.mean(X)
Y_mean=np.mean(Y)
for i in range(len(X)):
  num+=(X[i]-X_mean)*(Y[i]-Y_mean)
  deno+=(X[i]-X_mean)**2
m=num/deno
b=Y_mean-m*X_mean
print(m,b)
Y_pred=m*X+b
print(Y_pred)

plt.scatter(X,Y,color="red")
plt.plot(X,Y_pred)
plt.xlabel("Hour of Sunshine")
plt.ylabel("Ice Cream sold")
plt.show()
```

## Output
<img width="941" height="507" alt="image" src="https://github.com/user-attachments/assets/c643dc74-0c15-460e-8fa1-1f426861e79a" />
<img width="732" height="549" alt="image" src="https://github.com/user-attachments/assets/0fa3f7a7-4e54-4149-b558-d0b9026286d8" />


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
