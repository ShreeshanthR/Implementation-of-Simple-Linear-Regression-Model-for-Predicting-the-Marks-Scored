# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Take input data and create the Linear Regression model.
2. Train the model using the given X and Y values.
3. Predict marks for the entered study hours.
4. Plot the actual data and regression line.

## Program:
```python
'''
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: Shreeshanth R
RegisterNumber:  212225040411
'''

import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression
X = np.array(eval(input())).reshape(-1,1)
Y = np.array(eval(input()))

model = LinearRegression()
model.fit(X,Y)

x_input = float(input("ENTER HOURS STUDIED: "))
predicted_marks = model.predict([[x_input]])
print("Predicted Marks: ",predicted_marks[0])

y_pred = model.predict(X)
plt.scatter(X,Y,label="Actual Data")
plt.plot(X,y_pred,label="Regression Line")
plt.xlabel("HOURS STUDIED")
plt.ylabel("MARKS SCORED")
plt.title("SIMPLE LINEAR REGRESSION (USING SKLEARN)")
plt.legend()
plt.show()
```

## Output:
![simple linear regression model for predicting the marks scored](sam.png)

<img width="797" height="682" alt="ex2 ml graph" src="https://github.com/user-attachments/assets/0620a915-5afc-4091-85ba-df79b958579b" />

<img width="1002" height="126" alt="Screenshot 2026-09-01 195433" src="https://github.com/user-attachments/assets/bf5b172e-0d05-4732-aec3-e1717f2595fc" />


## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
