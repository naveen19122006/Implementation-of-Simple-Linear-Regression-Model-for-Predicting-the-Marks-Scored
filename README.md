# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Read the independent variable 𝑋 (study hours) and dependent variable 𝑌 (marks scored).

2.Calculate the mean of 𝑋 and the mean of 𝑌.

3.Compute the slope 𝑚 using

<img width="280" height="64" alt="image" src="https://github.com/user-attachments/assets/1261cb5d-d39f-4715-9e1e-58aff0f64260" />

4. Calculate the intercept 𝑏 using

<img width="131" height="38" alt="image" src="https://github.com/user-attachments/assets/a7d69651-1a70-4846-8603-ab0f1eb8eaef" />

5. Form the regression equation 𝑌=𝑚𝑋+𝑏 and predict the marks.


## Program:
```python
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: NAVEEN KUMAR E 
RegisterNumber:  212224230181
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
<img width="630" height="490" alt="image" src="https://github.com/user-attachments/assets/6dc84d01-419c-4872-86fd-803b39fed05d" />



## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
