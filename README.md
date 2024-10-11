# EX 6 Implementation of Decision Tree Classifier Model for Predicting Employee Churn
# DATE:
## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries.
2. Upload and read the dataset.
3. Check for any null values using the isnull() function.
4. Find the accuracy of the model and predict the required values by importing the required module from sklearn.

## Program:
```

Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: K DEEKSHITHA
RegisterNumber:  2305002005

import pandas as pd
from sklearn.tree import DecisionTreeClassifier,plot_tree
from sklearn.preprocessing import LabelEncoder
import matplotlib.pyplot as plt
df=pd.read_csv('/content/Employee_EX6.csv')
data = pd.read_csv('/content/Employee_EX6.csv')
data = df.copy()
data
le = LabelEncoder()
data['salary'] = le.fit_transform(data['salary'])
data
X = data.drop(['Departments','left'],axis=1)
Y = data['left']
clf = DecisionTreeClassifier()
clf.fit(X,Y)
plt.figure(figsize=(80,80))
plot_tree(clf, feature_names=X.columns,class_names=['LEFT','"NOT LEFT"'],filled=True,fontsize=14)
plt.show()
```

## Output:
![image](https://github.com/user-attachments/assets/63c47140-dd6f-4d53-9b70-83ca0c53e82d)
![image](https://github.com/user-attachments/assets/65356873-2789-4f1a-8c88-a00b89fe1b36)
![image](https://github.com/user-attachments/assets/16a8d292-a640-4d6c-865c-e33c8588e396)
![image](https://github.com/user-attachments/assets/a9c9c19e-1ad8-432d-abf8-cb662281656f)

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
