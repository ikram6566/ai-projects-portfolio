# Online Shoppers Purchasing Intention

**Result: 89.9% accuracy** (Random Forest) · buyer recall 53.2% · Logistic Regression 85.6% · always-"no purchase" baseline 84.5%.

## The project
Predict whether an e-commerce session ends in a purchase, from the UCI Online Shoppers dataset — **12,330 real sessions**, of which 15.5% converted. Features are behavioural: pages viewed (administrative / informational / product), dwell times, bounce and exit rates, PageValues, plus month, visitor type and weekend flag.

## Method
1. Load from the UCI archive; one-hot encode month / visitor type / weekend.
2. Random Forest (200 trees) vs class-weighted Logistic Regression, stratified 75/25 split.
3. Report accuracy **and buyer recall** — with 84.5% of sessions not buying, accuracy alone flatters. Confusion matrix saved as `confusion_matrix.png`.

## What I learned
PageValues dominates the prediction, and the honest metric for a shop is how many real buyers you catch (recall), not the headline accuracy.

## Run it
Open `online_shoppers_intention.ipynb` in Google Colab or locally — it downloads the dataset itself.
