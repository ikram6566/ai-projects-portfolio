# 52 · Sonar Mines vs Rocks Classification

**Result: 86.5% accuracy (Random Forest) · Logistic Regression 82.7% · always predicting the majority class (mine) scores 53.8% on the test set.**

## The problem
A sonar pulse bounced off a metal cylinder (a mine) returns a different energy pattern across 60 frequency bands than one bounced off a roughly cylindrical rock. With only 208 signals, this classic benchmark asks whether 60 numbers are enough to tell mine from rock.

## Data
UCI Connectionist Bench (Sonar, Mines vs. Rocks) (id 151) — 208 signals, 60 features. No missing values.

## Classes
- M (mine, metal cylinder): 111 signals
- R (rock): 97 signals

## Honest note
Small and noisy: only 52 signals are in the test set, so each signal is worth about 1.9 percentage points. The forest gets every mine in the test set right but misses about 29% of rocks, so the errors are one-sided — read the confusion matrix, not just the headline.

## Approach
- Stratified 75/25 split
- Random Forest (300 trees) vs scaled logistic regression

## Run it
Open `sonar_classification.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

![Confusion matrix](confusion_matrix.png)

## Stack
Python · pandas · scikit-learn · matplotlib
