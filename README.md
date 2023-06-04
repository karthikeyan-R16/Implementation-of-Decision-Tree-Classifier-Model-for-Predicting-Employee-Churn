# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
1.Import the required libraries.
2.Upload and read the dataset.
3.Check for any null values using the isnull() function.
4.From sklearn.tree import DecisionTreeClassifier and use criterion as entropy.
5.Find the accuracy of the model and predict the required values by importing the required module from sklearn.
```

## Program:
```
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Karthikeyan R
RegisterNumber:  212222240045

import pandas as pd
data=pd.read_csv("/content/Employee.csv")

print('data.info:')
data.info()

print('data.isnull().sum():')
data.isnull().sum()

print('value_count: ')
data["left"].value_counts()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()

data["salary"]=le.fit_transform(data["salary"])
data.head()

*x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()**

y=data["left"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)

from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy

dt.predict([[0.5,0.8,9,260,6,0,1,2]])
```

## Output:

![ml6](https://github.com/karthikeyan-R16/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119421232/b0944312-45ca-4b5a-ab4c-888bd4cdacb6)

![ml6 1](https://github.com/karthikeyan-R16/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119421232/5a4160fd-4d15-4904-bbbc-c1b064e25a32)

![ml6 2](https://github.com/karthikeyan-R16/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119421232/f54b8d17-efcf-4334-81a4-e0813f60cbc5)

![ml6 3](https://github.com/karthikeyan-R16/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119421232/9b065292-dd32-4cf2-bb7e-993c534a6f7a)

![ml6 4](https://github.com/karthikeyan-R16/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119421232/f7251299-4aa1-418b-812f-5c35276bfd34)

![ml6 5](https://github.com/karthikeyan-R16/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119421232/d0d65970-34eb-4abf-8e60-7477d3866b94)


![ml6 6](https://github.com/karthikeyan-R16/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119421232/9961a896-3b07-45d4-84e8-fec1f7e2824d)

![ml6 7](https://github.com/karthikeyan-R16/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119421232/5d03de5b-2a45-4d33-b8fa-7cb7e71e8f52)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
