#  Vox Connect: AI-Powered Health Assistant

Vox Connect is a machine learning–driven chatbot designed to assist clinics, hospitals, and municipal health centers by predicting illnesses based on patient symptom data. Built for real-world deployment, it supports both `.pkl` and `.onnx` formats for flexible integration across platforms.

---

##  Purpose

To provide fast, accurate illness predictions using supervised machine learning, improving triage, patient experience, and operational efficiency in healthcare settings.

---

##  Features

- Predicts diagnosis labels (e.g., Flu, Hypertension, Skin Allergy)
- Supports multiple ML models: Logistic Regression, Decision Tree, Random Forest
- Uses structured symptom data including age, duration, and severity
- Exportable to `.pkl` (Python) or `.onnx` (cross-platform) formats
- Ready for integration into chatbots, web apps, or edge devices

---

##  Training Data

- **Sources**: Synthetic datasets + public repositories (e.g., Disease Symptom Prediction)
- **Labels**: Predefined illness categories
- **Features Used**:
  - Symptoms (binary/categorical)
  - Age (numeric)
  - Duration (days)
  - Severity (ordinal)

---

##  Model Pipeline

1. **Data Preprocessing**: Encoding, normalization, missing value handling
2. **Model Training**: Choose from Logistic Regression, Decision Tree, or Random Forest
3. **Evaluation**: Accuracy, precision, recall, F1-score, confusion matrix
4. **Export**: Save model as `.pkl` or `.onnx` for deployment

---

##  Installation

```bash
# Clone the repository
git clone https://github.com/BUSINESS-AI-PROJECT/Vox-Connect-.git
cd vox-connect

# Install dependencies
pip install -r requirements.txt
