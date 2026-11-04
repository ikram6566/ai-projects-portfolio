# 60 · Haberman Survival Classification

**Result: 74.0% accuracy (Logistic Regression) · Random Forest 68.8% · always predicting the majority outcome (survived) also scores 74.0% on the test set.**

## The problem
306 breast-cancer surgery patients, each described by just three numbers: age at operation, year of operation, and the number of positive axillary lymph nodes detected. Predict whether the patient survived five years or longer — a deliberately hard, small, imbalanced problem.

## Data
UCI Haberman's Survival (id 43) — 306 patients, 3 features. No missing values.

## Classes
- survived 5+ years: 225 patients
- died within 5 years: 81 patients

## Honest note
Stated plainly: the best model here does not beat the naive baseline. Logistic Regression at 74.0% gets exactly the same number of test patients right as always predicting 'survived' (57 of 77), and the forest is worse than that baseline. With only three features, survival after surgery is largely unpredictable in this dataset, and the minority class (died) is recalled at only about a third. This is a weak result, and it is reported as one.

## Approach
- Stratified 75/25 split
- Random Forest (300 trees) vs scaled logistic regression

## Run it
Open `haberman_survival.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

![Confusion matrix](confusion_matrix.png)

## Stack
Python · pandas · scikit-learn · matplotlib
