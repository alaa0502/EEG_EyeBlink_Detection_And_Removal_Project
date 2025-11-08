# EEG Eye-Blink Artifact Cleaner — in three steps only

1. Upload your EEG (.edf)  
2. Click Start  
3. Download your cleaned .edf file  

---

## About this tool

Eye-blink artifacts (and artifacts in general) are common in EEG recordings and are usually not relevant to brain activity.  
They often need to be removed manually, which is time-consuming and requires experience.

This tool provides a simple and accessible solution:

- No need to code or preprocess manually.
- Just upload an `.edf` file, choose cleaning strictness, and get a cleaned version.

### Important limitation
This tool is currently most suitable for **students or introductory use**.

The model is trained mainly on involuntary eye-blink activity from **Fp1 and Fp2** channels.  
It is **not yet** trained on voluntary eye movements, other ocular artifacts, muscle (EMG) noise, or environmental noise.

Since I work with diverse EEG recordings, there is potential for gradual refinement of the model to include additional artifact types over time.

---

## Try it online

**Web App:**  
https://eye-artifact-cleaner.streamlit.app/

---

##  Demo 
![App Demo](./demopic.png)


---

## Run Locally (Optional)

```bash
# (Optional) Create a virtual environment
python -m venv .venv

# Activate:
# Windows:
. .venv\Scripts\activate
# macOS / Linux:
source .venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run the app
streamlit run artifact_app.py
