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
> Use a *stable* URL from the Issue (click the video → **Open original** / **Copy link**).  
> Avoid temporary `private-user-images?...jwt=` links — they expire.

```html
<video src="PASTE-STABLE-VIDEO-URL.mp4" controls playsinline width="720" poster="docs/thumb.png"></video>
