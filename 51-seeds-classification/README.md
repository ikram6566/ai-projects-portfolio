# 51 · Seeds Wheat Variety Classification

**Result: 94.3% accuracy (Logistic Regression) · Random Forest 84.9% · always predicting a majority variety scores 34.0% on the test set.**

## The problem
Wheat kernels from three varieties look alike to the eye, but seven geometric measurements of each kernel — area, perimeter, compactness, length, width, asymmetry and groove length, measured from soft X-ray images — separate them surprisingly well. This project predicts the variety from those seven numbers alone.

## Data
UCI Seeds (id 236) — 210 kernels, 7 features. No missing values.

## Classes
- Kama: 70 kernels
- Rosa: 70 kernels
- Canadian: 70 kernels

## Honest note
This is a small dataset — only 53 kernels land in the test set, so a single kernel is worth about 1.9 percentage points and the headline should not be read as precise to the last decimal. That said, the gap between the two models is large: the scaled linear model separates these varieties far better than the forest here, and Rosa is perfectly separated in the test set while Kama and Canadian are confused with each other.

## Approach
- Stratified 75/25 split
- Random Forest (300 trees) vs scaled logistic regression

## Run it
Open `seeds_classification.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

![Confusion matrix](confusion_matrix.png)

## Stack
Python · pandas · scikit-learn · matplotlib
