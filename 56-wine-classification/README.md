# 56 · Wine Cultivar Classification

**Result: 100% accuracy (Random Forest and Logistic Regression tied) · always predicting the majority cultivar scores 40.0% on the test set.**

## The problem
Three cultivars of wine grown in the same region of Italy, each described by 13 chemical measurements — alcohol, malic acid, ash, alkalinity, magnesium, phenols, flavanoids and more. With only 178 wines, can chemistry alone tell which cultivar a wine came from?

## Data
UCI Wine (id 109) — 178 wines, 13 features. No missing values. This is a different dataset from Wine Quality (project 09), which covers Portuguese wines.

## Classes
- Cultivar 1: 59 wines
- Cultivar 2: 71 wines
- Cultivar 3: 48 wines

## Honest note
A perfect score on 45 test wines is not proof of a perfect model: the classes are chemically well separated and the test set is small, so 100% here means 'separated on this split', not 'will never err'. Both models agree on every test wine, which is reassuring, but a new vintage could still surprise them.

## Approach
- Stratified 75/25 split
- Random Forest (300 trees) vs scaled logistic regression

## Run it
Open `wine_classification.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

![Confusion matrix](confusion_matrix.png)

## Stack
Python · pandas · scikit-learn · matplotlib
