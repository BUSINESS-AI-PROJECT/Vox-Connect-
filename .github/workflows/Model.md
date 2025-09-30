#  Model — Vox Connect AI

The Vox Connect AI model is a supervised machine learning classifier designed to predict likely illnesses based on patient-reported symptoms, age, and symptom duration. It powers the autonomous triage machine by converting structured input into actionable medical guidance.

---

##  Model Type

- **Multi-class classification**
- Predicts one of several possible diagnoses
- Trained using:
  - Random Forest (default)
  - Logistic Regression (baseline)
  - Naive Bayes (lightweight)
  - Optional: Support Vector Machine (SVM) for high-dimensional symptom vectors

---

##  Input Features

| Feature     | Type     | Description                                  |
|-------------|----------|----------------------------------------------|
| `symptoms`  | Text     | List of symptoms reported by the patient     |
| `age`       | Integer  | Patient age in years                         |
| `duration`  | String   | Duration of symptoms (e.g., "3 days")        |

---

##  Output

- **Diagnosis**: Predicted illness label (e.g., "Influenza", "Gastroenteritis")
- **Confidence Score**: Used to determine referral certainty
- **Referral Mapping**: Links diagnosis to clinic room or specialist

---

##  Training Process

- Text features vectorized using Bag-of-Words or TF-IDF
- Age and duration normalized and merged with symptom vectors
- Model trained on labeled dataset using 80/20 train-test split
- Evaluation metrics:
  - Accuracy
  - Precision
  - Recall
  - F1 Score
  - Confusion Matrix

---

##  Deployment Format

- Exported as `.pkl` using `joblib`
- Vectorizer saved alongside model for consistent input formatting
- Integrated into kiosk interface for real-time predictions
- Compatible with Raspberry Pi, Jetson Nano, and offline environments

---

##  Continuous Improvement

- Logs anonymized patient interactions for retraining
- Time series analysis triggers model updates
- Feedback loop from clinic staff improves contextual accuracy
- Threshold tuning balances sensitivity and specificity

---

##  Benefits

- Fast and interpretable predictions
- Lightweight enough for edge devices
- Adaptable to multilingual and voice-based input
- Designed for real-world deployment in low-resource clinics

