# EEG Eye-Blink Detection and Removal Tool

Artifact is a signal caused by an extracerebral source, observed during EEG recording, and is considered unwanted information (noise) in brain studies.  
The common approach to removing artifacts is done manually by researchers, which is time-consuming and requires expertise.  
Therefore, a tool that performs this process automatically is needed.

This web app is designed to provide a friendly, automatic, and reliable solution for (currently) non-expert use and students.  
Simply upload an EEG (.edf) file, choose the strictness of cleaning (default or fine-tuned), and click **Start**.  
A cleaned version of the data will then be available for download.

**Use directly in the browser (no installation needed):**  
https://eye-artifact-cleaner.streamlit.app/

---

## 🎥 Demo
<video
  src="https://alaa0502.github.io/detection_removel_eye_artifacts/demo.mp4"
  type="video/mp4"
  controls
  playsinline
  width="720">
</video>

---

## Running Locally (optional)

If you only want to use the online version, **you can skip this section**.

The installation below is for users who wish to run or modify the app locally (e.g., for research labs, offline use, or development).

```bash
# (Optional) Create a virtual environment
python -m venv .venv

# Activate
# Windows:
. .venv\Scripts\activate
# macOS / Linux:
source .venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run the app
streamlit run artifact_app.py
