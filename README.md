Artifact is a signal, caused by an extracerebral source, observed during EEG recording and is considered unwanted information (noise) in brain studies.
 The common method of removing artifacts is done manually by researchers and is time- and effort-consuming.
 Therefore, a tool that performs this automatically is needed.
 
This web app is provided to offer a friendly, automatic, and reliable tool for (currently) non-expert use and students.
 All that is required is to upload an EEG file, choose the strictness of cleaning (default or fine-tuned), and click Start. A cleaned version of the data is then made available for download, ready for use.
 
 visit:[https: //eye-artifact-cleaner.streamlit.app/](https://eye-artifact-cleaner.streamlit.app/)
 ## 🎥 Demo
<video src="https://github.com/alaa0502/detection_removel_eye_artifacts/issues/1#issue-3497113306.mp4" controls playsinline width="720"></video>
<video src="https://github.com/alaa0502/detection_removel_eye_artifacts/issues/1#issue-3497113306.mp4" controls playsinline poster="docs/thumb.png" width="720"></video>


 
The tool’s parameters were carefully chosen after a training process using different methods (RNN, CNNs) and were tested with real data and are supported by scientific studies.

However, it is still under development to match professional use, since training was performed mainly on data selected from Fp1 and Fp2 channels (sufficient for blink artifacts). Coverage is planned to be expanded to all eye artifacts (voluntary and involuntary), and then to be extended gradually to other physiological, technical, and environmental artifacts.

To keep things simple, all information is included in the repo as follows:

to get the code of the app use:artifact_app.py

to get the ML model of eye artifct detection used in the app, use:final model.py

to get a reflection of my process while developing the model use:best model.ipynb-colab.pdf
