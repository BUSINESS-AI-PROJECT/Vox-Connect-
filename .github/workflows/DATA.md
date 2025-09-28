#  Data Relevance to Vox Connect AI
Vox Connect AI is designed to predict illnesses and guide patients in clinical settings. To achieve this, the system relies on structured, medically relevant data that directly supports its supervised learning and NLP components. Below is a breakdown of each data type used, its relevance, and an example.

## 1. Symptom Descriptions (Textual Input)
Purpose: Captures patient-reported symptoms in natural language.

Relevance: Forms the core input for both NLP and illness prediction.

**Example:**

```python
"symptoms": ["fever", "cough", "fatigue"]
```

Source: Synthetic entries, MedSymptomDB, WHO symptom lists.

## 2. Patient Demographics (Numerical Input)

Purpose: Adds context to symptom severity and diagnosis likelihood.

Relevance: Age and duration influence disease probability and urgency.

**Example:**

```python
"age": 34,
"duration": "3 days"
```

Source: Synthetic data modeled on MIMIC-III and local clinic patterns.

## 3. Diagnosis Labels (Categorical Output)
Purpose: Supervised learning target for training the model.

Relevance: Enables the model to learn symptom-to-illness mappings.

**Example:**

```python
"diagnosis": "Influenza"
```
Source: Labeled datasets, WHO mappings, local triage protocols.


##  4. Referral Mapping (Operational Logic)
Purpose: Links predicted illness to appropriate specialist or room.

Relevance: Powers the kiosk’s guidance and referral system.

**Example:**

```python
"diagnosis": "Influenza" → "General Practitioner" → "Room 3"
```
Source: Local clinic layouts, municipal health guidelines.

## 5. NLP Vocabulary (Language Model Support)
Purpose: Enables accurate symptom extraction from patient input.

Relevance: Supports multilingual and low-literacy environments.

**Example:**

```txt
Vocabulary: ["rash", "itching", "redness", "fever", "sore throat"]
```
Source: Curated from MedSymptomDB, WHO symptom lists, and community feedback.

## Summary
Each data type is:

* Directly tied to the solution’s goals (triage, prediction, referral)

* Structured for supervised learning and NLP

* Ethically sourced or synthetically generated

* Designed for real-world deployment in clinics and municipal centers
  
