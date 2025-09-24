# Vox Connect AI Machine

**Vox Connect AI Machine** is a smart health kiosk designed to assist patients in clinics and municipal health centers. It uses supervised machine learning and natural language processing to interpret symptoms, predict illnesses, recommend specialists, and guide patients to the correct department, all through a touchscreen interface.

---

## 🧠 Core Features

1. **Patient Input**  
   Accepts symptom descriptions via touchscreen or voice.

2. **Symptom Analysis**  
   Uses NLP to extract and categorize symptoms.

3. **Illness Prediction**  
   Predicts likely conditions using supervised machine learning.

4. **Doctor Referral**  
   Recommends the appropriate specialist based on predicted illness.

5. **Room Guidance**  
   Directs patients to the correct department.

---

## 🏥 Use Case

Vox Connect AI is ideal for:
- Public clinics with high patient volume  
- Municipal health centers with limited staff  
- Hospitals seeking to automate triage and reduce wait times

---

## 🧰 Hardware Setup

- Raspberry Pi or Jetson Nano  
- 7" Touchscreen Display  
- Optional Microphone (for voice input)  
- Local storage (SQLite or flat files)  
- Durable kiosk casing with signage

---

## 🧪 Machine Learning Model

- **Type:** Supervised learning (Logistic Regression / Decision Tree / Random Forest)  
- **Inputs:** Symptoms, age, duration  
- **Output:** Predicted diagnosis  
- **Training Data:** Synthetic + public datasets (e.g., MedSymptomDB, MIMIC-III)  
- **Deployment Format:** `.pkl` or `.onnx` model file

---



