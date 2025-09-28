# Machine Learning Approach — Vox Connect AI 

Vox Connect AI uses a supervised machine learning pipeline to predict illnesses based on patient-reported symptoms. The system is designed for real-time triage in clinics and municipal health centers, with a focus on speed, interpretability, and offline deployment.

## Problem Framing
- **Type:** Multi-class classification
- **Input:** Patient symptoms, age, duration
- **Output:** Predicted diagnosis (e.g., Influenza, Hypertension, Skin Allergy)

## Dataset Summary
**Each training entry includes:**
```json
{
  "symptoms": ["fever", "cough", "fatigue"],
  "age": 34,
  "duration": "3 days",
  "diagnosis": "Influenza"
}
