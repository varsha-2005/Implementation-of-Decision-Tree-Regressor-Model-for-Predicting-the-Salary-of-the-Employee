# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the libraries and read the data frame using pandas.
2. Calculate the null values present in the dataset and apply label encoder.
3. Determine test and training data set and apply decison tree regression in dataset.
4. calculate Mean square error,data prediction and r2.
## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: varsha.g
RegisterNumber:  212222230166
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
data.head()

![image](https://github.com/Thenmozhi-Palanisamy/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/95198708/48e17f09-8429-4ac5-8fe2-ee44d76fb21a)


data.info()

![image](https://github.com/Thenmozhi-Palanisamy/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/95198708/c4648e85-9777-4f19-b846-8b1df6a47967)

isnull() and sum()

![image](https://github.com/Thenmozhi-Palanisamy/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/95198708/3aba0d79-e0d6-41ea-bc5d-2f1bd94f8b87)

data.head() for salary

![image](https://github.com/Thenmozhi-Palanisamy/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/95198708/747bdff3-543f-413f-b005-8d2921f227f1)

MSE value

![image](https://github.com/Thenmozhi-Palanisamy/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/95198708/8499df80-847c-4498-b250-f30050c8b58f)

r2 value

![image](https://github.com/Thenmozhi-Palanisamy/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/95198708/c932496c-87d7-4794-a4a4-807bc4931939)

data prediction

![image](https://github.com/Thenmozhi-Palanisamy/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/95198708/a79326e7-b16b-4cc8-aaf3-229fe12b7537)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
