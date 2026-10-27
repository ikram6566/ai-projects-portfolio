# 31 · Airfoil Self-Noise Prediction

**Result: R² 0.932, MAE 1.32 dB** (Random Forest) · Linear Regression R² 0.518.

## The problem
Quieter aircraft and wind turbines start in the wind tunnel. NASA measured 1,503 airfoil configurations; given the test conditions, predict the noise (scaled sound pressure level, dB).

## Data
UCI Airfoil Self-Noise (NASA) — 1503 runs; features: frequency, angle of attack, chord length, free-stream velocity, suction-side displacement thickness.

## Approach
- 75/25 train-test split
- Random Forest (300 trees) vs a scaled linear baseline

## What the model shows
Velocity and frequency dominate the noise — physically sensible, since aerodynamic noise scales steeply with flow speed.

## Run it
Open `airfoil_noise_prediction.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

## Stack
Python · pandas · scikit-learn · matplotlib
