# 67 · Landsat Satellite Classification

**Result: 90.9% accuracy (Random Forest) · Logistic Regression 85.5% · always predicting the majority class (red soil) scores 23.8% on the test set.**

## The problem
6,435 pixels from satellite images, each described by 36 multi-spectral values from a 3x3 neighbourhood. Predict the land-cover class of the central pixel — red soil, cotton crop, grey soil, damp grey soil, soil with vegetation stubble, or very damp grey soil.

## Data
UCI Statlog (Landsat Satellite) (id 146) — 6,435 pixels, 36 features. No missing values. Class 6 is absent from this dataset, so only 6 classes appear.

## Classes
- 1 (red soil): 1,533 pixels
- 2 (cotton crop): 703 pixels
- 3 (grey soil): 1,358 pixels
- 4 (damp grey soil): 626 pixels
- 5 (soil with vegetation stubble): 707 pixels
- 7 (very damp grey soil): 1,508 pixels

## Honest note
The weak spot is damp grey soil (class 4), recalled at only 56% — it is confused with the other grey soils, which is physically plausible, since the classes differ mainly in dampness. The other five classes are all recognised at 88% or better.

## Approach
- Stratified 75/25 split
- Random Forest (300 trees) vs scaled logistic regression

## Run it
Open `landsat_satellite.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

![Confusion matrix](confusion_matrix.png)

## Stack
Python · pandas · scikit-learn · matplotlib
