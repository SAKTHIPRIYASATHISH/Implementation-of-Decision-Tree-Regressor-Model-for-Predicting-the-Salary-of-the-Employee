# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas
2.Import Decision tree classifier 
3.Fit the data in the model 
4..Find the accuracy score 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: S.Sakthi Priya
RegisterNumber:212222040140  
*/
import pandas as pd
data=pd.read_csv("salary.csv")
data.head()
data.info()
data.isnull().sum()
 from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
data.info()
x=data[["Position","Level" ]]
x.head()
y=data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test= train_test_split(x,y,test_size=0.2,random_state=100)
x_train.shape
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
```

## Output:
df.head()

![s1](https://github.com/SAKTHIPRIYASATHISH/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119104282/0bd4bea3-1dc9-4563-9302-00015d091b9b)


df.info()

![s2](https://github.com/SAKTHIPRIYASATHISH/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119104282/2f2249e0-1883-40a9-aa64-00ec229c9f25)


df.isnull.sum()

![s3](https://github.com/SAKTHIPRIYASATHISH/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119104282/67f9a1ae-910f-402e-b050-a5c71318231e)

after label encoding



![s4](https://github.com/SAKTHIPRIYASATHISH/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119104282/8307107d-331c-421f-a917-7c2c3b83a16e)

x_train.shape


![s5](https://github.com/SAKTHIPRIYASATHISH/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119104282/20c86191-7d1d-48ce-9b9f-b32701cb4094)

y_pred


![s6](https://github.com/SAKTHIPRIYASATHISH/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119104282/46fdaed5-18ae-4cfa-b55a-9c3293d049e7)


MSE value


![s7](https://github.com/SAKTHIPRIYASATHISH/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119104282/26055e58-ffdb-4e3b-996e-d82f20efb63e)


R2 value


![s8](https://github.com/SAKTHIPRIYASATHISH/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119104282/5ffa5945-a9ac-4641-8b9b-6d3ead97cb7e)


predicted value


![s9](https://github.com/SAKTHIPRIYASATHISH/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119104282/f7915907-d9ce-4d70-8975-a5f7ece14019)











## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
