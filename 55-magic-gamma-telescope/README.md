# 55 · MAGIC Gamma Telescope Classification

**Result: 88.4% accuracy (Random Forest) · Logistic Regression 79.8% · always predicting the majority class (gamma) scores 64.8% on the test set.**

## The problem
The MAGIC telescope records showers of particles in the atmosphere. Gamma-ray showers (the signal astronomers want) must be separated from hadron showers (the background) using 10 image-shape measurements of each shower. With 19,020 events, this is the largest dataset in this batch.

## Data
UCI MAGIC Gamma Telescope (id 159) — 19,020 events, 10 features. No missing values.

## Classes
- gamma (signal): 12,332 events
- hadron (background): 6,688 events

## Honest note
The headline hides a real asymmetry: the forest recalls 94% of gamma events but only 78% of hadron events, so about one in five background showers is mistaken for signal. For a telescope, that false-signal rate matters more than the overall accuracy, and the linear model is clearly weaker here (79.8%) — the boundary is not linear.

## Approach
- Stratified 75/25 split
- Random Forest (300 trees) vs scaled logistic regression

## Run it
Open `magic_gamma_telescope.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

![Confusion matrix](confusion_matrix.png)

## Stack
Python · pandas · scikit-learn · matplotlib
