# Bank Marketing Prediction

Predicts whether a bank client will subscribe to a term deposit after a phone marketing campaign, using the **UCI Bank Marketing** dataset (45,211 real clients; only 11.7% subscribed).

## Verified result (executed notebook)
- **Random Forest: 90.8% accuracy** ✅ best
- Logistic Regression: 90.2%

## Run it
Open `bank_marketing_prediction.ipynb` — it downloads the dataset itself from UCI and runs end to end.

## Honest note
With an 11.7% "yes" rate, a lazy model that always says "no" already scores 88.3% — so the headline accuracy flatters every model here. The notebook prints the full classification report (precision/recall for the subscribing class) and a confusion matrix, which is where the real performance lives.

## Why it matters
Call-centre time is money. Ranking clients by subscription likelihood lets a bank call the most promising 20% first instead of dialling the whole list.
