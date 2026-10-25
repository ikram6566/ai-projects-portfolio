# Census Income Prediction (Adult)

**Result: 84.3% accuracy** (Random Forest) · Logistic Regression 84.7% · majority baseline 75.1%.

## The project
Predict whether a person earns over $50K/year, from the UCI Adult / Census Income dataset — 30,162 complete records from the 1994 US Census (demographics, education, occupation, hours, capital gains/losses).

## Method
1. Load `adult.data` from the UCI archive; '?' → NaN → drop incomplete rows; drop `fnlwgt` (a survey weight, not a personal feature).
2. One-hot encode categoricals; stratified 75/25 split.
3. Random Forest (200 trees) vs scaled Logistic Regression; confusion matrix saved as `confusion_matrix.png`.

## Honest note
The census features include protected attributes (sex, race, native country). This is a learning project on public data — a real system making decisions about people would need a bias audit and, usually, those features removed.

## Run it
Open `census_income_prediction.ipynb` in Google Colab or locally — it downloads the dataset itself.
