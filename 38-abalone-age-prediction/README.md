# 38 · Abalone Age Prediction

**Result: R² 0.537, MAE 1.55 rings** (Random Forest) · Linear Regression R² 0.545.

## The problem
Counting shell rings under a microscope is the accurate way to age an abalone — and the slow way. Can size and weight measurements replace it?

## Data
UCI Abalone — 4177 specimens; sex, length, diameter, height and four weights. Target: number of rings.

## Honest note
This dataset is famous for being *hard*: physical measurements only partially determine age, and published R² values cluster where this model lands. The gap between "easy-looking" and "actually predictable" is the lesson.

## Run it
Open `abalone_age_prediction.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

## Stack
Python · pandas · scikit-learn · matplotlib
