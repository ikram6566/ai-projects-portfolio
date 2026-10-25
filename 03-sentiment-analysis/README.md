# Sentiment Analysis 💬

Reading a short review and deciding whether it is **positive** or **negative** — the same technology businesses use to monitor customer feedback at scale.

## Result
**Accuracy: 82.2%** on 550 held-out reviews (2,748 usable labelled sentences from IMDb, Yelp and Amazon — UCI Sentiment Labelled Sentences dataset).

Demo (from the notebook):
- POSITIVE ← "This product is amazing, I absolutely love it!"
- NEGATIVE ← "Worst experience ever, the food was cold and the staff was rude."
- POSITIVE ← "The movie was brilliant, great acting and a beautiful story."
- NEGATIVE ← "Total waste of money, I will never buy this again."

## How it works
1. Combine the IMDb, Yelp and Amazon labelled-sentence files; drop rows corrupted by stray tab characters
2. Convert text to TF-IDF features (1–2 word phrases, 5,000 features) so "not good" is captured as one signal
3. Train Logistic Regression on an 80/20 stratified split
4. Evaluate (accuracy, precision, recall, F1) and test on fresh sentences

## Why it matters
This exact workflow powers review monitoring, customer-feedback dashboards and brand-sentiment tracking for marketing teams.

## Run it
Open `sentiment_analysis.ipynb` in Jupyter or Google Colab and run all cells — the notebook downloads the dataset itself.

**Tools:** Python, pandas, scikit-learn (TF-IDF + Logistic Regression)
