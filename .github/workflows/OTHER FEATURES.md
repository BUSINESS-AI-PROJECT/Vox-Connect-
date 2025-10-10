# Vox Connect AI Chat-Bot Solution

The chatbot serves as the primary interface between patients and the Vox Connect system. It replaces traditional intake staff by:

- Accepting patient input via text or voice

- Asking structured follow-up questions to clarify symptoms

- Interpreting natural language using NLP

- Triggering illness prediction and referral logic

- Providing spoken or visual guidance to the correct room or department

This makes it essential for:

- Reducing wait times

- Improving triage accuracy

- Enabling autonomous operation in clinics with limited staff

- Supporting multilingual and low-literacy populations

## Well-Planned Architecture

The chatbot is designed with modular components that reflect real-world clinic needs:

|Module	|Functionality|
|---------|------|
|NLP Engine |	Extracts symptoms and context from patient input|
|Dialogue Manager |	Guides patients through structured symptom reporting|
|Prediction Trigger	| Sends extracted data to ML model for diagnosis|
|Referral Logic |	Maps diagnosis to correct specialist and room|
|Multilingual Layer	| Supports English, isiZulu, Afrikaans (extensible)|
|Voice Integration	| Optional speech input/output for accessibility|
|Fallback Routing	| Refers to general practitioner if prediction confidence is low|

## Appropriately Setup for Clinics

- **Offline-capable:** Runs on Raspberry Pi or Jetson Nano without internet

- **Touchscreen-friendly:** Designed for kiosk interaction

- **Voice-enabled:** Uses speech recognition and synthesis for accessibility

- **Privacy-conscious:** No personal data stored; logs are anonymized

- **Scalable:** Can be deployed across multiple clinics with minimal configuration

## Example Interaction Flow

```plaintext
🤖 Vox Connect AI:
Hello! What symptoms are you experiencing today?

👤 Patient:
I’ve had a sore throat and fever for three days.

🤖 Vox Connect AI:
Thank you. Based on your symptoms, you may have Influenza.
Please proceed to Room 3 to see the General Practitioner.
```
## Summary
The chatbot/softbot feature is:

- Highly relevant to autonomous triage and patient intake

- Well-planned with modular, scalable architecture

- Appropriately setup for offline, multilingual, and inclusive deployment

- Achievable using open-source tools and lightweight hardware
