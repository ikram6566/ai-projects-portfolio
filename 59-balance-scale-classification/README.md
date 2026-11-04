# 59 · Balance Scale Classification

**Result: 86.6% accuracy (Logistic Regression) · Random Forest 80.9% · always predicting a majority outcome scores 46.5% on the test set.**

## The problem
A balance scale tips left, tips right, or stays balanced depending on the weight and distance on each side. The physics is a simple product — left weight times left distance versus right weight times right distance — but can a generic classifier learn that product rule from 625 examples?

## Data
UCI Balance Scale (id 12) — 625 scales, 4 features. No missing values. The class is the first column in this file.

## Classes
- L (tips left): 288 scales
- R (tips right): 288 scales
- B (balanced): 49 scales

## Honest note
Neither model learns the product rule cleanly, and the balanced class is the casualty: it has only 49 examples in the whole dataset (12 in the test set), and the Random Forest misses every single one of them. The headline is carried by the two tipping classes; balanced scales are the hard, rare case here, and a model that used the actual torque product would beat both of these.

## Approach
- Stratified 75/25 split
- Random Forest (300 trees) vs scaled logistic regression

## Run it
Open `balance_scale_classification.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

![Confusion matrix](confusion_matrix.png)

## Stack
Python · pandas · scikit-learn · matplotlib
