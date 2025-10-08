# Eye-Artifact Cleaner (EEG) — Blink/Saccade Noise Removal

A simple, friendly web app for **automatic eye-artifact detection and attenuation** in EEG recordings.  
Designed for students and non-experts; useful as a fast first pass before deeper analysis.

🔗 **Live app:** https://eye-artifact-cleaner.streamlit.app

---

## Why?
An **artifact** is a signal caused by an **extracerebral** source (e.g., eye blinks/saccades) that appears in EEG and is considered unwanted noise in brain studies.  
Manual cleaning is still common and can be **time- and effort-consuming**. This project provides an **automatic** alternative with a simple UI.

---

## What it does
- Upload an EEG file (currently **EDF** tested)
- Choose cleaning **strictness** (default or fine-tuned)
- Click **Start**
- Download the **cleaned** EEG file for immediate use

> ⚠️ **Note:** The current model is trained primarily on **Fp1/Fp2** channels (well suited for blink artifacts). Broader coverage is planned (see Roadmap).

---
## 🎥 Demo
[▶️ Watch the demo (opens the Issue)](https://github.com/alaa0502/detection_removel_eye_artifacts/issues/1#issue-3497113306)

<video src="https://private-user-images.githubusercontent.com/112955765/499098929-985e69b1-c512-41fa-8e5a-7501371acf7c.mp4?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9..." controls playsinline width="720"></video>

