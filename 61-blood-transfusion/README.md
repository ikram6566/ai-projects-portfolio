# 61 · Blood Transfusion Service Classification

**Result: 77.0% accuracy (Logistic Regression) · Random Forest 70.6% · always predicting the majority outcome (did not donate again) scores 76.5% on the test set.**

## The problem
748 blood donors, each described by four numbers: months since the last donation (Recency), total number of donations (Frequency), total blood donated in c.c. (Monetary), and months since the first donation (Time). Predict whether the donor gave blood again in March 2007.

## Data
UCI Blood Transfusion Service Center (id 176) — 748 donors, 4 features. No missing values.

## Classes
- Did not donate again: 570 donors
- Donated again: 178 donors

## Honest note
This is a weak result, stated plainly: the best model at 77.0% beats the naive majority baseline by only half a percentage point on 187 test donors, and the forest is worse than that baseline. Repeat donors are recalled at only about a third, so four donation-history numbers do not predict a return visit well.

## Approach
- Stratified 75/25 split
- Random Forest (300 trees) vs scaled logistic regression

## Run it
Open `blood_transfusion.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

![Confusion matrix](confusion_matrix.png)

## Stack
Python · pandas · scikit-learn · matplotlib
