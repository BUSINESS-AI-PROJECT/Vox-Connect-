# Machine Learning Approach — Vox Connect AI 

Vox Connect AI uses a supervised machine learning pipeline to predict illnesses based on patient-reported symptoms. The system is designed for real-time triage in clinics and municipal health centers, with a focus on speed, interpretability, and offline deployment.

## Problem Framing
- **Type:** Multi-class classification

- **Input:** Patient symptoms, age, duration

- **Output:** Predicted diagnosis (e.g., Influenza, Hypertension, Skin Allergy)

## Dataset Summary
**Each training entry includes:**

```python
{
  "symptoms": ["fever", "cough", "fatigue"],
  "age": 34,
  "duration": "3 days",
  "diagnosis": "Influenza"
}
```
* _Sources: Synthetic records, MedSymptomDB, MIMIC-III, WHO mappings_

* _Preprocessing: Tokenization, vectorization, one-hot encoding of labels_

## Algorithm Selection

|Algorithm	|Reason for Use|
|-------------|------------|
|Logistic Regression	| Fast, interpretable baseline|
|Decision Tree	| Rule-based logic, easy to visualize|
|Random Forest	| Handles noisy data, improves accuracy|
|Naive Bayes	| Lightweight, good for text-based symptom input|
|Optional: MLP	| For deeper pattern recognition (if hardware allows)|

## Feature Engineering
- **Symptoms:** Tokenized and vectorized using TF-IDF or Bag-of-Words

- **Age & Duration:** Normalized numeric inputs

- **Severity (optional):** Derived from symptom intensity keywords

- **Language Support:** NLP pipeline built for English, with plans for isiZulu and Afrikaans

## Training Pipeline

- **Data Cleaning:** Remove duplicates, normalize formats

- **Split:** 80/20 train-test split

- **Model Training:** Fit selected algorithms

- **Evaluation:** Accuracy, precision, recall, confusion matrix

- **Export:** Save best model as .pkl or .onnx for deployment

## Deployment Strategy

- **Environment:** Raspberry Pi or Jetson Nano

- **Interface:** Python-based UI with real-time prediction

- **Offline Capability:** No cloud dependency; runs locally

- **Fallback Logic:** If prediction confidence is low, refer to general practitioner

## Benefits of This Approach

- Transparent and explainable predictions

- Fast inference on low-power hardware

- Easy to retrain with new labeled data

- Aligns with ethical AI principles in healthcare

  ---
