# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Load the placement dataset using the Pandas library.

2.Create a copy of the dataset and remove unnecessary columns like serial number and salary.

3.Check the dataset for missing values and duplicate records.

4.Convert all categorical attributes into numerical form using Label Encoding.

5.Separate the dataset into independent features (X) and target variable (status).

6.Split the dataset into training and testing sets using an 80:20 ratio.

7.Initialize the Logistic Regression model with a suitable solver.

8.Train the model using the training dataset.

9.Predict the placement status using the test dataset.

10.Evaluate the model performance using accuracy score and classification report.

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: vignesh.K
RegisterNumber:  212225240183
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression

data = pd.read_csv("Untitled.csv")

data = data.drop("salary", axis=1)
data = pd.get_dummies(data, drop_first=True
X = data.drop("status_Placed", axis=1)
y = data["status_Placed"]
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
model = LogisticRegression(max_iter=1000)
model.fit(X_train, y_train)
print("Accuracy:", model.score(X_test, y_test))
 
X1 = X.iloc[:, 0].values.reshape(-1, 1)

model_plot = LogisticRegression(max_iter=1000)
model_plot.fit(X1, y)

plt.scatter(X1, y, color='blue')

x_values = np.linspace(X1.min(), X1.max(), 100)
y_values = model_plot.predict_proba(x_values.reshape(-1,1))[:,1]

plt.plot(x_values, y_values)

plt.xlabel("Feature")
plt.ylabel("Probability")
plt.title("Logistic Regression Curve")
plt.show()

*/
```

## Output:
 <img width="772" height="611" alt="Screenshot 2026-04-28 093833" src="https://github.com/user-attachments/assets/fe16eb0a-b32d-430a-9dba-0d60377d9f20" />



## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
