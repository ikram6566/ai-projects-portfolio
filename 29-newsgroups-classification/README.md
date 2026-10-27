# 20 Newsgroups Topic Classification

**Result: 82.6% accuracy** (TF-IDF + Logistic Regression, 20 classes).

## The project
Assign Usenet posts to their newsgroup — space, hockey, cryptography, religion, and 16 more — from text alone. The classic 20 Newsgroups corpus: 11,314 training posts and 7,532 test posts on the standard chronological split.

## Method
1. Load via scikit-learn's `fetch_20newsgroups` (standard train/test split).
2. TF-IDF (30,000 features, 1–2 grams, sublinear) + Logistic Regression.
3. The residual errors are the genuinely overlapping pairs (politics/religion, Mac/Windows hardware).

## Run it
Open `newsgroups_classification.ipynb` in Google Colab or locally — it downloads the corpus itself.
