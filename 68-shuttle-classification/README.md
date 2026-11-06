# 68 · Shuttle Classification

**Result: 99.9% accuracy (Random Forest) · Logistic Regression 96.6% · always predicting the majority class scores 78.6% on the test set.**

## The problem
58,000 space-shuttle radiator and engine readings, each described by 7 sensor values. Predict the shuttle's state — a famously imbalanced dataset where one class holds almost 80% of all examples and three classes have fewer than 200 examples between them.

## Data
UCI Statlog (Shuttle) (id 148) — 58,000 readings, 7 features. No missing values.

## Classes
- Class 1: 45,586 readings
- Class 2: 50 readings
- Class 3: 171 readings
- Class 4: 8,903 readings
- Class 5: 3,267 readings
- Class 6: 10 readings
- Class 7: 13 readings

## Honest note
The headline is real for the big classes — the forest is essentially perfect on the 11,396 class-1 and 2,226 class-4 test readings — but it says nothing about the rare classes: class 6 has only 3 test readings and is missed entirely, and class 7 has only 3 test readings with one correct. Those per-class scores are meaningless at this sample size, and the headline should not be quoted without that caveat.

## Approach
- Stratified 75/25 split
- Random Forest (300 trees) vs scaled logistic regression

## Run it
Open `shuttle_classification.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

![Confusion matrix](confusion_matrix.png)

## Stack
Python · pandas · scikit-learn · matplotlib
