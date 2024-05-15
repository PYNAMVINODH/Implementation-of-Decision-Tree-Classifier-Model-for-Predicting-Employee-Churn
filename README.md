# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1. Import the required libraries.
   
2. Upload and read the dataset.
   
3. Check for any null values using the isnull() function.
   
4. From sklearn.tree import DecisionTreeClassifier and use criterion as entropy.
   
5. Find the accuracy of the model and predict the required values by importing the required module from sklearn.

## Program:
```
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: PYNAM VINODH
RegisterNumber: 212223240131
```
```py
import pandas as pd
df=pd.read_csv("Employee.csv")

df.head()
df.info()
df.isnull().sum()
df["left"].value_counts()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()

df["salary"]=le.fit_transform(df["salary"])
df.head()

x=df[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()

y=df["left"]

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

### data.head()

![image](https://github.com/PYNAMVINODH/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145742678/7b658467-64cd-416b-8d43-bcc6b50d247a)


### data.info()

![image](https://github.com/PYNAMVINODH/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145742678/91c0b972-d4cf-4f1c-8a70-43f4874a3985)


### isnull() and sum()

![image](https://github.com/PYNAMVINODH/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145742678/ec3c304c-9eec-4963-bbe2-6ced3b4acf34)


### data value counts()

![image](https://github.com/PYNAMVINODH/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145742678/7802d1e6-92d9-45e6-aa2d-b1226f48ddbf)



### data.head() for salary

![image](https://github.com/PYNAMVINODH/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145742678/62cd34a8-83d7-459a-8600-cf4473067034)


### x.head()

![image](https://github.com/PYNAMVINODH/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145742678/c9a79145-2d0b-47ee-a187-863f96e4a527)


### accuracy value

![image](https://github.com/PYNAMVINODH/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145742678/2ca5e806-dd7a-4943-b1a2-39f9d14f03d8)

### data prediction

![image](https://github.com/PYNAMVINODH/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145742678/82bd7882-2e79-4f59-bb0d-48202637b39f)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
