# 70 · Mammographic Mass Classification

**Result: 81.7% accuracy (Logistic Regression) · Random Forest 78.4% · always predicting the majority outcome (benign) scores 53.5% on the test set. Educational only — not a medical tool.**

## The problem
961 mammographic masses, each described by BI-RADS assessment, patient age, mass shape, margin and density. Predict severity — benign or malignant.

## Data
UCI Mammographic Mass (id 161) — 961 masses, 5 features. 162 missing values across the feature columns, filled with the training-set median per column. Note: this dataset's target column is 'Severity', not 'class', in the UCI CSV.

## Classes
- Benign (0): 516 masses
- Malignant (1): 445 masses

## Honest note
This is a genuinely hard, noisy clinical problem: even the best model here misses about 15% of malignant masses and 27% of benign ones on 241 test masses. That error rate would be unacceptable as a diagnostic tool, which is why this project is educational only — it shows what five coarse mammographic features can and cannot do.

## Approach
- Stratified 75/25 split
- Random Forest (300 trees) vs scaled logistic regression

## Run it
Open `mammographic_mass.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

![Confusion matrix](confusion_matrix.png)

## Stack
Python · pandas · scikit-learn · matplotlib
