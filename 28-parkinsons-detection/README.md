# Parkinson's Detection from Voice Measurements

**Result: 93.9% accuracy** (Logistic Regression) · Random Forest 91.8% · Parkinson's recall 97.3%.

## The project
Classify voice recordings as healthy or Parkinson's from 22 acoustic measurements (pitch, jitter, shimmer, noise ratios). UCI Parkinsons dataset: 195 recordings, 147 of them from patients.

## The honest caveat (read this first)
The 195 recordings come from only **31 people**, and a random split puts the same person's voice in both train and test — so this score is optimistic versus testing on brand-new patients. It demonstrates that voice carries disease signal; it is **not** a diagnostic tool and validates nothing clinically.

## Method
1. Load from the UCI archive; scale the 22 voice features.
2. Logistic Regression vs Random Forest, stratified 75/25 split; confusion matrix saved as `confusion_matrix.png`.

## Run it
Open `parkinsons_detection.ipynb` in Google Colab or locally — it downloads the dataset itself.
