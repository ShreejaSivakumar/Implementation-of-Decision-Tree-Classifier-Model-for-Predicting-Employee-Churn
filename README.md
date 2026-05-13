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
Developed by: SHREEJA R S
RegisterNumber:  25017561
*/

import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier, plot_tree
from sklearn.metrics import accuracy_score, classification_report

# 1. Load the dataset
data = pd.read_csv("Employee.csv")

# 2. Separate features and target BEFORE encoding
X = data.iloc[:, :-1]   # All columns except last
y = data.iloc[:, -1]    # Last column (target)

# 3. One-hot encode only the features (X)
X = pd.get_dummies(X, drop_first=True)

# 4. Split into training and testing sets
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# 5. Train the Decision Tree Classifier
model = DecisionTreeClassifier(random_state=42)
model.fit(X_train, y_train)

# 6. Predict and Evaluate
y_pred = model.predict(X_test)

print("=" * 45)
print("         DECISION TREE - RESULTS")
print("=" * 45)
print(f"\n✅ Accuracy : {accuracy_score(y_test, y_pred) * 100:.2f}%")
print("\n📊 Classification Report:")
print("-" * 45)
print(classification_report(y_test, y_pred))

# 7. Visualize the Decision Tree
plt.figure(figsize=(22, 10))
plot_tree(
    model,
    feature_names=X.columns.tolist(),         # ✅ Fix: convert to list
    class_names=[str(c) for c in model.classes_],  # ✅ Fix: class names
    filled=True,
    rounded=True,
    fontsize=9
)
plt.title("Decision Tree Classifier - Employee Leave Prediction",
          fontsize=16, fontweight='bold')
plt.tight_layout()
plt.savefig("decision_tree.png", dpi=150, bbox_inches='tight')
plt.show()

```

## Output:
![decision tree classifier model](sam.png)

<img width="762" height="458" alt="Screenshot_13-5-2026_133717_localhost" src="https://github.com/user-attachments/assets/538e5a02-6067-4a37-bdc0-c020f3917135" />


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










