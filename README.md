# End-to-End Independent Final Project – Data Science Course

## EEG Eye-Blink Artifact Cleaner App — in three steps only

1) Upload your `.edf` file
2) Select detection strictness or leave default
3) Download the cleaned EEG file

---
## why this tool matters

Unlike EEGLAB’s manual or ICA-based review, this tool uses a lightweight ML approach to automatically remove blink artifacts, reducing manual cleaning time and improving consistency. 
Currently focused on blink artifacts only.

---

## About this tool

This project focuses on removing eye-blink artifacts from EEG signals in a simple and accessible way. 
Eye blinks introduce high-amplitude noise in frontal EEG channels (commonly Fp1/Fp2), which can distort neural signal analysis. 
The tool automatically detects blink intervals and attenuates their effect, allowing cleaner downstream processing.
This tool provides a simple and accessible solution:

- No need to code or preprocess manually.
- Just upload an `.edf` file, choose cleaning strictness, and get a cleaned version.

## Inspiration
  
During my practicum in neuroscience, I cleaned EEG data manually and noticed how time-consuming that step can be. 
I decided to dedicate my final end-to-end project in Data Science to exploring an automated approach to this problem.

---

## limitation of use

This tool is designed to automate the reduction of blink artifacts in the frontal EEG channels (Fp1 and Fp2), where blink-related activity is most strongly represented. Because the model is trained specifically on this channel configuration and artifact type, the tool is currently most appropriate for student use, introductory preprocessing, or quick data cleaning prior to more advanced workflows. Other artifacts (such as muscle activity, voluntary eye movement, and motion-related noise) require different labeling strategies, channel selections, and model designs, so they are not included here; however, the pipeline is modular, and others may extend it to additional artifact classes if desired.

---

## Why Start With Blink Artifacts?

Blink artifacts were selected as the starting point because they produce a characteristic frontally distributed signal pattern caused by the oculomotor dipole, which can be isolated in channels such as Fp1 and Fp2 without requiring full multi-channel modeling. In contrast, developing a general artifact-cleaning tool requires treating each artifact type as a separate supervised ML problem, with its own annotation criteria, channel dependence, feature representation, and validation procedure. Beginning with blink artifacts therefore provides a focused and methodologically appropriate foundation before extending automated preprocessing to additional artifact classes.

---

## Try it online

**Web App:**  
https://eye-artifact-cleaner.streamlit.app/

---

##  Demo 
![App Demo](./demopic.png)


---
## project structure

artifact_app.py → Streamlit web app (upload → clean → download)

final_model.py → Final blink-detection + cleaning functions used in the app

best model.ipynb-colab.pdf → Machine learning model development (visualizations of tests and tuning are included)

requirements.txt → Python library dependencies

README.md → Project explanation and usage instructions

## how to insert it

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

---

## requirements

streamlit>=1.32
mne>=1.5
scikit-learn>=1.3
numpy>=1.23
plotly>=5.15
edfio
