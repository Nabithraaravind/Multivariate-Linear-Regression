# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import pandas module. Import linear_model from sklearn

### Step2
Read the csv file (saved in the same directory) using pd.read_csv.

### Step3
Prepare regression using linear_model.LinearRegression() and assign it to identifier "regr".

### Step4
The coefficients can be obtained by regr.coef_ and the intercept can be obtained by regr.intercept_. The predicted result can be obtained by regr.predict().

### Step5
Print the output and end the program.

## Program:
```
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
x = df[['Weight','Volume']]
y = df['CO2']
regr=linear_model.LinearRegression()
regr.fit(x,y)
print ("Coefficients:",regr.coef_)
print ("Intercept:",regr.intercept_)
input_data=pd.DataFrame({'Weight':[3300],'Volume':[1300]})
PredictedCO2=regr.predict(input_data)
print ("Predicted CO2 for the corresponding Weight and Volume:",PredictedCO2)

```
## Output:

![Screenshot 2024-12-10 162651](https://github.com/user-attachments/assets/5f091dfd-94c0-4135-8479-c170f5c80c0f)

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
