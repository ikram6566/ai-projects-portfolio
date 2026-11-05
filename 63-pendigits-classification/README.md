# 63 · Pen Digits Classification

**Result: 99.1% accuracy (Random Forest) · Logistic Regression 94.5% · always predicting any single digit scores about 10.4% on the test set, since the digits are balanced.**

## The problem
10,992 handwritten digits, each written with a pen on a tablet and described by 16 spatial coordinates of the pen trajectory. Predict the digit (0-9) from the trajectory alone — a harder cousin of the pixel-based MNIST projects.

## Data
UCI Pen-Based Recognition of Handwritten Digits (id 81) — 10,992 samples, 16 features. No missing values. Note: this dataset's target column is capitalised 'Class' in the UCI CSV.

## Classes
- Digits 0-9: roughly 1,050-1,144 samples each (see notebook output for exact counts)

## Honest note
With 2,748 test samples, 99.1% is a solid, well-measured result, not a small-sample fluke — every digit is recognised at 96% or better by the forest. The linear model is clearly weaker (94.5%), so the trajectory boundary is not linear.

## Approach
- Stratified 75/25 split
- Random Forest (300 trees) vs scaled logistic regression

## Run it
Open `pendigits_classification.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

![Confusion matrix](confusion_matrix.png)

## Stack
Python · pandas · scikit-learn · matplotlib
