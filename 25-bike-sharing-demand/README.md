# Bike Sharing Demand Prediction

**Result: R² 0.918, MAE 33.2 bikes/hour** (Random Forest) vs 141 bikes/hour for the always-average baseline.

## The project
Predict hourly bike rentals for Washington DC's Capital Bikeshare (2011–2012, 17,379 hours) from weather, season, hour and day type — the forecast an operator needs to rebalance bikes across stations.

## Method
1. Load `hour.csv` from the UCI archive.
2. One-hot encode calendar/weather categories. **Leakage excluded:** `casual` and `registered` sum exactly to the target `cnt`, so they are dropped — including them would fake a near-perfect score.
3. Random Forest regressor (200 trees), 75/25 split; hour of day is the dominant feature (commuter peaks).

## Honest note
A random split is optimistic for time-series data; a chronological split is the stricter follow-up and is discussed in the notebook.

## Run it
Open `bike_sharing_demand.ipynb` in Google Colab or locally — it downloads the dataset itself.
