# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import Libraries:,Load Data:
2. Encode Categorical Data:Use LabelEncoder to convert the categorical variable 'salary' into numerical format.
3. Define Features and Target:Select the relevant columns as features (X) and the target variable (y).
4. split the data using test_train_split
5. Initialize Model:
6. Make Predictions:
7. Evaluate Model:
8. Predict on New Data:



## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: PYNAM VINODH
RegisterNumber:  212223240131
import pandas as pd
data=pd.read_csv('Employee.csv')
print(data.head())
print(data.tail())
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()
y=data["left"]
y
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
*/
```

## Output:
### Data:
![image](https://github.com/PYNAMVINODH/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145742678/33b15cbb-de26-4ed7-9ebb-97ab2547f457)

### Encoder:
![image](https://github.com/PYNAMVINODH/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145742678/e2646409-8668-4678-885c-c06510247733)

### X-values and y-values
![image](https://github.com/PYNAMVINODH/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145742678/0cb12a63-c06c-4c2a-83ff-6f3cc9fa67fd)

![image](https://github.com/PYNAMVINODH/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145742678/14eeed26-f6df-4f7c-8ec3-b542b4a1352c)

### Accuracy and Prediction
![image](https://github.com/PYNAMVINODH/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145742678/5bf15b5b-870a-44d0-9e37-3be33d11141b)





## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
