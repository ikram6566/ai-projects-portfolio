# 66 · Optical Digits Classification

**Result: 98.9% accuracy (Random Forest) · Logistic Regression 97.2% · always predicting any single digit scores about 10.2% on the test set, since the digits are balanced.**

## The problem
5,620 handwritten digits, each as an 8x8 image flattened into 64 pixel values (0-16). Predict the digit (0-9) from the pixels alone — the classic small-image benchmark that predates MNIST.

## Data
UCI Optical Recognition of Handwritten Digits (id 80) — 5,620 samples, 64 features. No missing values.

## Classes
- Digits 0-9: 554-572 samples each (see notebook output for exact counts)

## Honest note
With 1,405 test samples, 98.9% is well measured — every digit is recognised at 96% or better by the forest. The linear model is a little weaker (97.2%), but the gap is small here, unlike the pen-trajectory digits in project 63.

## Approach
- Stratified 75/25 split
- Random Forest (300 trees) vs scaled logistic regression

## Run it
Open `optical_digits.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

![Confusion matrix](confusion_matrix.png)

## Stack
Python · pandas · scikit-learn · matplotlib
