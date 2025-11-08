# EEG Eye-Blink Artifact Cleaner

**Upload your EEG (.edf) → Click Start → Download a cleaner signal.**  
Removes involuntary **eye-blink artifacts** automatically, with the option to fine-tune cleaning strength.  
Visualize, clean, and continue your analysis with less noise and more confidence.

---

## Why this tool?
Eye-blink artifacts are common in EEG recordings and are not related to brain activity.  
They usually need to be removed **manually**, which is time-consuming and requires experience.

This tool provides a **simple and accessible** solution:
- No need to code or preprocess manually.
- Just upload an `.edf` file, choose cleaning strictness, and get a cleaned version.
- Designed mainly for **students, learning labs, and early-stage EEG work**.

**Important limitation:**  
The current model is trained mainly on **eye-blink activity from Fp1 and Fp2 channels**.  
It does **not yet cover** voluntary eye movement artifacts, muscle (EMG) noise, or environmental noise.  
Future development aims to expand the training set to support **clinical and professional research workflows**.

---

## Try it online (no installation needed)

**Web App:**  
https://eye-artifact-cleaner.streamlit.app/

---

## 🎥 Demo
*(If the preview does not load, open in browser.)*

<video
  src="https://alaa0502.github.io/detection_removel_eye_artifacts/demo.mp4"
  type="video/mp4"
  controls
  playsinline
  width="720">
</video>

---

## Run Locally (Optional)

If you want to run or modify the tool on your machine (e.g., research, offline use, development), follow:

```bash
# (Optional) Create a virtual environment
python -m venv .venv

# Activate it:
# Windows:
. .venv\Scripts\activate
# macOS / Linux:
source .venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Start the web app locally
streamlit run artifact_app.py

---
## requrements

streamlit>=1.32
mne>=1.5
scikit-learn>=1.3
numpy>=1.23
plotly>=5.15
edfio
 ---
##project structure

artifact_app.py              → Streamlit app (Upload → Clean → Download)
final_model.py               → Eye-blink detection + cleaning logic
best model.ipynb-colab.pdf   → Model development and reasoning notes

##
