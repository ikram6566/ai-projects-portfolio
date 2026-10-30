# 44 · Online News Popularity Prediction

**Result: R² 0.158 on log(shares), MAE 2,355 shares on the raw scale** (Random Forest) · Linear Regression R² 0.126, MAE 2,371 · always predicting the median scores MAE 2,422.

## The problem
Editors would love to know which articles will travel. This dataset (Mashable, 2013–2015) asks how much of an article's eventual share count is predictable from features available *before* publication.

## Data
UCI Online News Popularity — 39644 articles in the shipped file, 58 numeric predictors after dropping `url` and `timedelta`. Target: `shares`.

## Approach
- Shares are heavily right-skewed, so the modelling target is `log1p(shares)`; R² is reported on that log scale
- Predictions are converted back with `expm1` and MAE is also reported on the original share scale
- 75/25 split; Random Forest regressor (200 trees) vs scaled linear regression

## Honest note
Virality is mostly *not* in the pre-publication features — an R² around this level is what the research literature on this dataset finds too. The model ranks articles better than chance; it does not foresee hits.

## Run it
Open `online_news_popularity.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

## Stack
Python · pandas · scikit-learn · matplotlib
