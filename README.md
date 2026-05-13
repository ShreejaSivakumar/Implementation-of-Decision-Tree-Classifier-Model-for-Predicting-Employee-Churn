# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn


# DATE : 13/05/2026

# NAME : SHREEJA R S
# REG.NO : 25017561

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1. **Load** → Read CSV, split into features (X) and target (y)
2. **Encode** → Convert text columns to numbers using one-hot encoding
3. **Split** → 80% train, 20% test
4. **Train** → Feed training data into the Decision Tree
5. **Predict** → Test the model, check accuracy score
6. **Visualize** → Draw and save the tree as an image 

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: 
RegisterNumber:  
*/


import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier, plot_tree
from sklearn.metrics import accuracy_score
# 1. Load the dataset
data = pd.read_csv("Employee.csv")
# 2. Separate features and target BEFORE encoding
#    Assumes the last column is the target (e.g., 'LeaveOrNot')
X = data.iloc[:, :-1]   # All columns except the last
y = data.iloc[:, -1]    # Last column (target)
# 3. One-hot encode only the FEATURES (X), not the target (y)
X = pd.get_dummies(X, drop_first=True)
# 4. Split into training and testing sets
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)
# 5. Train the Decision Tree model
model = DecisionTreeClassifier(random_state=42)
model.fit(X_train, y_train)
# 6. Predict and evaluate
y_pred = model.predict(X_test)
print("Accuracy:", accuracy_score(y_test, y_pred))
# 7. Visualize the Decision Tree
plt.figure(figsize=(20, 10))
plot_tree(
    model,
    feature_names=X.columns.tolist(),   # FIX: convert Index to list
    class_names=[str(c) for c in model.classes_],  # FIX: add class names
    filled=True,
    rounded=True,       # nicer look
    fontsize=10
)
plt.title("Decision Tree - Employee Leave Prediction")
plt.tight_layout()     # FIX: prevents label clipping
plt.savefig("decision_tree.png", dpi=150)  # optional: save the tree
plt.show()  


```

## Output:
![decision tree classifier model](sam.png)

<img width="804" height="182" alt="Screenshot_13-5-2026_131635_localhost" src="https://github.com/user-attachments/assets/44b781df-c3f6-4e5a-921d-0aa01ce92563" />


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .








































































































  ..
  .
  .
  ....
  .
  .
  ..
  .
  .
  .
  .
  .


  .
  .
  .
  .
  .
  .
  .

  ..
  .
  .










