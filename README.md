# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.  Import pandas library to read csv or excel file.

2. Import LabelEncoder using sklearn.preprocessing library.

3. Transform the data's using LabelEncoder.

4 . Import decision tree classifier from sklearn.tree library to predict the values.

5 . Find accuracy.

6 . Predict the values.

7 . End of the program.


## Program:
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Gayathri A
RegisterNumber:  212221230028
*/
```
import pandas as pd
data=pd.read_csv("Employee.csv")
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()
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
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
```

## Output:

![61](https://user-images.githubusercontent.com/94154854/204556642-356025af-5993-47ae-9f30-473e7dd365de.png)

![62](https://user-images.githubusercontent.com/94154854/204556682-7ba514a1-d553-4dfc-acaf-82fe9eef84d5.png)

![63](https://user-images.githubusercontent.com/94154854/204556729-8b226066-4e51-45e7-b297-eb52fa87f148.png)

![64](https://user-images.githubusercontent.com/94154854/204556773-06ead484-8536-4e4b-a221-c07e1c854339.png)

![65](https://user-images.githubusercontent.com/94154854/204556855-e4f373e5-8bd6-4d4f-8277-2959a5c03630.png)

![66](https://user-images.githubusercontent.com/94154854/204556880-d7a77353-f146-4c8a-8f71-a4fc68a37ee5.png)

![67](https://user-images.githubusercontent.com/94154854/204556926-b67fb832-48bf-4d86-9b4f-a0da79a2aedb.png)

![68](https://user-images.githubusercontent.com/94154854/204556979-b187c05c-0bb5-42d4-b023-7a3ed879795f.png)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
