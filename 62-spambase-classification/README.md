# 62 · Spambase Spam Classification

**Result: 95.3% accuracy (Random Forest) · Logistic Regression 92.8% · always predicting the majority class (not spam) scores 60.6% on the test set.**

## The problem
4,601 emails, each described by 57 word-frequency, character-frequency and capital-run-length features. Predict spam versus non-spam — the classic email-filtering benchmark, without reading any message text.

## Data
UCI Spambase (id 94) — 4,601 emails, 57 features. No missing values. Note: this dataset's target column is capitalised 'Class' in the UCI CSV.

## Classes
- Not spam: 2,788 emails
- Spam: 1,813 emails

## Honest note
Both models are genuinely strong here, with the forest recalling 92% of spam and 98% of non-spam on 1,151 test emails. The remaining spam errors are the costliest kind for a filter, but at this accuracy the trade-off is a small one.

## Approach
- Stratified 75/25 split
- Random Forest (300 trees) vs scaled logistic regression

## Run it
Open `spambase_classification.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

![Confusion matrix](confusion_matrix.png)

## Stack
Python · pandas · scikit-learn · matplotlib
