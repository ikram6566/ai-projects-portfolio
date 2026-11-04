# 58 · Dermatology Disease Classification

**Result: 96.7% accuracy (Random Forest and Logistic Regression tied) · always predicting the majority disease scores 30.4% on the test set.**

## The problem
Six erythemato-squamous skin diseases look similar on examination, but 34 clinical and histopathological features — erythema, scaling, itching, koebner phenomenon, melanin incontinence, fibrosis and more — separate them. Predict the disease from those features.

## Data
UCI Dermatology (id 33) — 366 patients, 34 features. 8 ages are missing and are filled with the training-set median, so no test information leaks.

## Classes
- Disease 1: 112 patients
- Disease 2: 61 patients
- Disease 3: 72 patients
- Disease 4: 49 patients
- Disease 5: 52 patients
- Disease 6: 20 patients

## Honest note
Both models agree at 96.7% on 92 test patients, with the remaining errors concentrated in diseases 2 and 4, which are the hardest to separate clinically. The small disease-6 class (5 test patients) is fully correct here, but five patients are too few to generalise from.

## Approach
- Stratified 75/25 split
- Random Forest (300 trees) vs scaled logistic regression

## Run it
Open `dermatology_classification.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

![Confusion matrix](confusion_matrix.png)

## Stack
Python · pandas · scikit-learn · matplotlib
