# 41 · Superconductor Critical Temperature Prediction

**Result: R² 0.925, MAE 5.18 K** (Random Forest) · Linear Regression R² 0.728, MAE 13.39 K.

## The problem
A superconductor's usefulness is set by its critical temperature: below it, resistance drops to zero. Screening candidate materials in the lab is slow and expensive, so a model that estimates critical temperature from a compound's composition is a genuine research tool.

## Data
UCI Superconductivity Data — 21263 materials, 81 features derived from the chemical formula (element proportions and weighted thermal-conductivity, valence-electron and atomic-mass statistics). Target: `critical_temp` in kelvin.

## Approach
- 75/25 split
- Random Forest regressor (300 trees) vs scaled linear regression

## Run it
Open `superconductor_temperature.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

## Stack
Python · pandas · scikit-learn · matplotlib
