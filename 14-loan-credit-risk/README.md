# Loan Credit-Risk Prediction

Predicts good vs bad credit risk — the scoring core of loan approval — using the classic **German Credit** dataset (UCI Statlog; 1,000 applicants, 20 features).

## Verified result (executed notebook)
- **Random Forest: 72.8% accuracy** ✅ best
- Logistic Regression: 72.4%

## Run it
Open `loan_credit_risk.ipynb` — it downloads the dataset from UCI itself and runs end to end.

## Honest note
~73% is the realistic ceiling for this small 1994 dataset. Real lending models use far more data, fairness testing and human review — this project teaches the pipeline, not a production decision engine.
