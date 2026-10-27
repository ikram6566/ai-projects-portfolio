# 33 · Beijing PM2.5 Air-Pollution Prediction

**Result: R² 0.840, MAE 22.3 µg/m³** (Random Forest) · Linear R² 0.273 · always-average MAE 68.8.

## The problem
PM2.5 particles are small enough to enter the bloodstream, so forecasting them matters. Given only the weather, how well can we predict the current hour's PM2.5 level?

## Data
UCI Beijing PM2.5 — 41757 hourly records with a pollution reading (2010–2014), weather features: dew point, temperature, pressure, wind direction/speed, snow and rain hours.

## Approach
- Records without a PM2.5 reading dropped; wind direction one-hot encoded
- Random 75/25 split; Random Forest (200 trees) vs scaled linear baseline and the always-average baseline

## Honest note
A random split lets the model see neighbouring hours in training, which flatters the score versus a true forecast. A production forecaster would split by time — the notebook's number is a "nowcast from weather" figure, not a next-day forecast.

## Run it
Open `beijing_pm25_prediction.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

## Stack
Python · pandas · scikit-learn · matplotlib
