# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
### Algorithm: Simple Linear Regression for Predicting Marks

1. Start

2. Enter the values of X (Hours Studied) and Y (Marks Scored).

3. Calculate the mean of X and Y.

   x_mean = sum(X) / n

   y_mean = sum(Y) / n

4. Calculate the slope:

   b1 = sum((X - x_mean) * (Y - y_mean)) / sum((X - x_mean)^2)

5. Calculate the intercept:

   b0 = y_mean - (b1 * x_mean)

6. Form the regression equation:

   Y = b0 + b1 * X

7. Enter the number of hours studied by a new student.

8. Predict the marks using:

   Predicted Marks = b0 + b1 * Hours

9. Display the predicted marks.

10. Plot the actual data points and regression line.

11. Stop.


## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: Mahalakshmi J
RegisterNumber:  212225230162
*/
```
```
import numpy as np
import matplotlib.pyplot as plt

# Input data
# Hours studied
X = np.array([1, 2, 3, 4, 5, 6, 7, 8])

# Marks scored
Y = np.array([35, 40, 50, 55, 65, 70, 80, 85])

# Calculate mean
x_mean = np.mean(X)
y_mean = np.mean(Y)

# Calculate slope (b1)
b1 = np.sum((X - x_mean) * (Y - y_mean)) / np.sum((X - x_mean) ** 2)

# Calculate intercept (b0)
b0 = y_mean - b1 * x_mean

# Predict marks
Y_pred = b0 + b1 * X

# Display regression equation
print("Slope (b1) =", b1)
print("Intercept (b0) =", b0)
print("Regression Equation: Marks =", b0, "+", b1, "* Hours")

# Predict marks for a new student
hours = float(input("Enter number of hours studied: "))
predicted_marks = b0 + b1 * hours

print("Predicted Marks =", predicted_marks)

# Plot data and regression line
plt.scatter(X, Y, label="Actual Marks")
plt.plot(X, Y_pred, label="Regression Line")

plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression - Marks Prediction")
plt.legend()
plt.show()

```

## Output:
![simple linear regression model for predicting the marks scored](sam.png)


## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
