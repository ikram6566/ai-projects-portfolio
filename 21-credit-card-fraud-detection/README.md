# Credit Card Fraud Detection

**Result: PR-AUC 0.704 · fraud recall 88.6% at 6.2% precision** (Logistic Regression, class-weighted) — accuracy 97.68% vs the 99.83% "always legitimate" baseline that catches zero fraud.

## The project
Detect fraudulent card transactions in the ULB dataset: **284,807 real transactions, only 492 of them fraud (0.17%)**. Features V1–V28 are published PCA components; `Time` and `Amount` are raw. Source: TensorFlow-hosted copy of the ULB Credit Card Fraud dataset.

## Why accuracy is the wrong headline here
A model that labels everything legitimate is right 99.83% of the time and useless. This project is therefore judged on:
- **PR-AUC (average precision): 0.704** — the honest metric at this prevalence
- **Fraud recall: 88.6%** of fraud caught
- **Fraud precision: 6.2%** of flags that were real fraud

## Method
1. Load the dataset; stratified 75/25 split.
2. Standardise features; Logistic Regression with `class_weight='balanced'` so the rare class counts.
3. Evaluate with PR-AUC / ROC-AUC (0.973), per-class report and a confusion matrix (saved as `confusion_matrix.png`).

## What I learned
- Class weighting trades false alarms for caught fraud — correct when a missed fraud costs more than a manual review.
- At 0.17% prevalence, ROC-AUC flatters; PR-AUC tells the truth.

## Run it
Open `credit_card_fraud_detection.ipynb` in Google Colab or locally — it downloads the dataset itself.
