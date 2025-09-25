## 1 Data cleaning  

df['symptoms'] = df['symptoms'].str.lower().str.replace('[^a-z, ]', '')
df.drop_duplicates(inplace=True)

---

## 2 Train-Test Split (80/20)

from sklearn.model_selection import train_test_split

X = df[['symptoms', 'age', 'duration']]
y = df['diagnosis']

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, stratify=y)

---

## 3 Model Training
 
Goal: Fit selected algorithms to the training data.

Algorithms Used:

Logistic Regression (baseline)

Decision Tree / Random Forest (for interpretability)

Naive Bayes (for text-heavy inputs)

Steps:

Vectorize symptoms using TF-IDF or Bag-of-Words.

Normalize numeric features (age, duration).

Encode diagnosis labels.

Train multiple models and compare performance.

from sklearn.ensemble import RandomForestClassifier
model = RandomForestClassifier()
model.fit(X_train_vectorized, y_train_encoded)
---
## 4 Evaluation

from sklearn.metrics import accuracy_score, precision_score, recall_score, confusion_matrix

y_pred = model.predict(X_test_vectorized)
print("Accuracy:", accuracy_score(y_test_encoded, y_pred))
print("Confusion Matrix:\n", confusion_matrix(y_test_encoded, y_pred))

---

## 5. Export Model

import joblib
joblib.dump(model, 'models/illness_predictor.pkl')

---
