# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm :
1. Import the required libraries .
2. Read the data frame using pandas.
3. Get the information regarding the null values present in the dataframe.
4. Apply label encoder to the non-numerical column inoreder to convert into numerical values.
5. Determine training and test data set.
6. Apply decision tree regression on to the dataframe.
7. Get the values of Mean square error, r2 and data prediction. 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: J,DEEPIKA
RegisterNumber: 212221230016

import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
x.head()
y=data[["Salary"]]
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
*/
```

## Output:

![1111111](https://user-images.githubusercontent.com/94747031/199080129-08c23b0a-5753-4b46-b14a-2fd729c0b4b3.png)

![22222222](https://user-images.githubusercontent.com/94747031/199080117-a18ec538-93db-4ff1-8c78-e8a03141f625.png)

![33333333](https://user-images.githubusercontent.com/94747031/199080111-12422941-f68e-4257-b08f-b78edb5bcb42.png)

![4444444](https://user-images.githubusercontent.com/94747031/199080100-9160946c-9b14-40dd-af80-ce6852114e0c.png)

![555555555](https://user-images.githubusercontent.com/94747031/199080154-4433c6e6-2075-4627-9cd2-f23e0cabd60f.png)

![66666666](https://user-images.githubusercontent.com/94747031/199080152-ca8fcc41-5eff-4c45-8a6c-427a42f5e09f.png)

![77777777](https://user-images.githubusercontent.com/94747031/199080146-94a4a4e0-3635-4557-978a-99f72ce97ad7.png)

![88888888](https://user-images.githubusercontent.com/94747031/199080140-2fca0e60-44a4-4496-8712-73a1b5880605.png)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
