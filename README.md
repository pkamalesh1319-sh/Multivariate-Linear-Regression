# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Start the program and import the required libraries, Pandas and Scikit-learn.

### Step2
Load the car emission dataset from the CSV file using pd.read_csv().

### Step3
Select Weight and Volume as input variables (X) and CO2 as the output variable (y).

### Step4
Create and train the Linear Regression model using LinearRegression() and fit().

### Step5
Predict the CO2 emission for Weight = 3300 and Volume = 1300, and display the coefficients, intercept, and predicted CO2 value.

## Program:
```
# Dataset Setup - Run this cell before starting the experiment

import pandas as pd

url = "https://raw.githubusercontent.com/arunpradeep-sec/Linear-Algebra-Lab/main/carsemission.csv"

df = pd.read_csv(url)
df.to_csv("carsemission.csv", index=False)

print("Dataset loaded successfully.")

#Developed by : Kamalesh P
#Register number : 26014307
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)

```
## Output:
<img width="1912" height="1047" alt="image" src="https://github.com/user-attachments/assets/4177ee77-3870-4905-bc55-533d90dafaaa" />

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
