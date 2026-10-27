# 32 · Building Energy Efficiency Prediction

**Result: R² 0.998, MAE 0.33** (Random Forest, heating load) · Linear Regression R² 0.915.

## The problem
Heating is one of the biggest costs of a building's life. From 768 simulated building designs, predict heating load from geometry and glazing alone — no physics simulation needed at run time.

## Data
UCI Energy Efficiency — 768 buildings × 8 design features (compactness, surface/wall/roof area, height, orientation, glazing).

## Approach
- 75/25 train-test split
- Random Forest (300 trees) vs scaled linear baseline

## Run it
Open `energy_efficiency_prediction.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

## Stack
Python · pandas · scikit-learn · matplotlib
