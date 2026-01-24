# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1.Initialize the given X and Y data values.
2.Calculate the mean values of X and Y.
3.Compute the slope (m) using the linear regression formula.
4.Calculate the intercept (b) and form the regression equation.
5.Plot the scatter diagram and draw the regression line.

## Program:
```python
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: NAVEEN KUMAR E
RegisterNumber: 212224230181 
*/

import matplotlib.pyplot as plt

X = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12]
Y = [18, 28, 35, 45, 52, 60, 68, 74, 79, 85, 90, 94]

n = len(X)

mean_x = sum(X) / n
mean_y = sum(Y) / n

num = 0
den = 0
for i in range(n):
    num += (X[i] - mean_x) * (Y[i] - mean_y)
    den += (X[i] - mean_x) ** 2

m = num / den
b = mean_y - m * mean_x

print(f"Y = {m:.2f}X + {b:.2f}")

y_pred = [m * x + b for x in X]

plt.scatter(X, Y)
plt.plot(X, y_pred)
plt.xlabel("Study Hours")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression with Realistic Data")
plt.show()

```

## Output:

<img width="630" height="490" alt="Screenshot 2026-01-22 162106" src="https://github.com/user-attachments/assets/d1f4d15c-3dc8-46b9-8d55-e06030aa2ff0" />


## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
