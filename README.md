# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.  Import the libraries and read the data frame using pandas.
2.  Calculate the null values present in the dataset and apply label encoder.
3.  Determine test and training data set and apply decison tree regression in dataset.
4.  calculate Mean square error,data prediction and r2.
   

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by:Tarun S
RegisterNumber:212223040226
*/

import pandas as pd
 data=pd.read_csv("C:/Users/admin/OneDrive/Desktop/Salary.csv")
 data.head()
 data.info()
 data.isnull().sum()
 from sklearn.preprocessing import LabelEncoder
 le=LabelEncoder()
 data['Position']=le.fit_transform(data['Position'])
 data.head()
 x=data[['Position','Level']]
 y=data['Salary']
 from sklearn.model_selection import train_test_split
 x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_stat
 from sklearn.tree import DecisionTreeClassifier
 dt=DecisionTreeClassifier()
 dt.fit(x_train,y_train)
 y_predict=dt.predict(x_test)
 from sklearn import metrics
 mse=metrics.mean_squared_error(y_test,y_predict)
 mse
 r2=metrics.r2_score(y_test,y_predict)
 r2
dt.predict([[5,6]])
 
 
```



## Output:
Data.head()

![image](https://github.com/Tarun-2006/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145584190/994592dc-9f22-4192-bb83-6f71ee06c332)

Data.info()

![image](https://github.com/Tarun-2006/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145584190/626a5a1a-767d-4a2d-bc8b-eb90157b0302)


#data.isnull().sum()

![image](https://github.com/Tarun-2006/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145584190/3736a074-b396-4fbc-9cd7-f0547de07918)

Data.Head() for salary:

![image](https://github.com/Tarun-2006/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145584190/d1aa07a9-c5d5-41d4-b1e3-83e444aaa348)

#MSE Value:

![image](https://github.com/Tarun-2006/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145584190/ac010e1d-7bfb-4cf1-ba94-64ba8fc97c3c)

#r2 Value:

![image](https://github.com/Tarun-2006/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145584190/51590383-299b-40dc-a94c-db4169b8607c)

#Data Prediction:

![image](https://github.com/Tarun-2006/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145584190/a2e00d7e-1401-4c93-8579-b21b90155e79)




## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.

