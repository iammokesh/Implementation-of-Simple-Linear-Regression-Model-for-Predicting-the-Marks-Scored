# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Input independent variable X and dependent variable Y.
2. Train a linear regression model using X and Y.
3. Extract slope m and intercept b to form equation Y=mX+b.
4.  Predict output for new input using the regression equation.
5.  Plot scatter points and regression line for visualization.


## Program:
```python
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: MOKESH C
RegisterNumber: 212225240088 
*/
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

# Sample data

X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
Y = np.array([35, 50, 65, 70, 85])

# Create model
model = LinearRegression()

# Train model
model.fit(X, Y)

# Get slope and intercept
m = model.coef_[0]
b = model.intercept_

print("Slope (m):", m)
print("Intercept (b):", b)

# ---- Prediction ----
x_input = float(input("Enter hours studied: "))
predicted_marks = model.predict([[x_input]])
print("Predicted Marks:", predicted_marks[0])

# ---- Plot ----
Y_pred = model.predict(X)

plt.scatter(X, Y, label="Actual Data")
plt.plot(X, Y_pred, label="Regression Line")
plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression (Using sklearn)")
plt.legend()
plt.show()
```

## Output:
<img width="912" height="728" alt="Screenshot 2026-04-24 160400" src="https://github.com/user-attachments/assets/df71f1a3-0629-42cb-8457-49db9dfa0ae5" />



## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
