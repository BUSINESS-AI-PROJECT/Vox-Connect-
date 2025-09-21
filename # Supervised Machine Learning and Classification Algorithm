# Supervised Machine Learning and Classification

# loading data:

# Install dependencies as needed:
pip install kagglehub[pandas-datasets]
py
import kagglehub
import pandas as pd
import numpy as np
from kagglehub import KaggleDatasetAdapter
 
file_path = "disease_symptoms.csv"
df = kagglehub.load_dataset(
  KaggleDatasetAdapter.PANDAS,
  "krish0202/symptom-based-disease-labeling-dataset",
  file_path
)

print("DataFrame info:", df.info())
print("\nFirst 5 records:", df.head())



# Separating features(independent variables to get predicted results):
y = df['Disease']

X = df.drop('Disease', axis=1)

print("\nFeatures (X) shape:", X.shape)
print("Target (y) shape:", y.shape)



# Handling categorical data:
X_encoded = pd.get_dummies(X, columns=X.columns)

print("\nEncoded features (X_encoded) shape:", X_encoded.shape)
print("First 5 encoded records:", X_encoded.head())



# Data splitting into training and testing datasets: data split into 80% for training and 20% for testing:

from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
    X_encoded, y, test_size=0.2, random_state=42
)

print("\nTraining set size:", len(X_train))
print("Testing set size:", len(X_test))



# Choosing and training a classification model by using a Decision tree classifier (Algorithm): (first initializing the model, and second training the model on the training data)

from sklearn.tree import DecisionTreeClassifier

model = DecisionTreeClassifier(random_state=42)

model.fit(X_train, y_train)

print("\nModel training complete.")



# Evaluating the model's performance: (step 1, making predictions on the test dataset, step 2, calculating the model's accuracy, 3 printing the report for detailed metrics)

from sklearn.metrics import accuracy_score, classification_report

y_pred = model.predict(X_test)

accuracy = accuracy_score(y_test, y_pred)
print(f"\nModel Accuracy: {accuracy:.4f}")

print("\nClassification Report:")
print(classification_report(y_test, y_pred, zero_division=0))



# New data prediction: (

new_data = pd.DataFrame(columns=X_encoded.columns, data=[[0]*len(X_encoded.columns)])
new_data['Symptom_headache'] = 1
new_data['Symptom_fever'] = 1

predicted_disease = model.predict(new_data)
print("\nPredicted disease for new sample:", predicted_disease[0])

