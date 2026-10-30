# 39 · Gas Turbine CO Emission Prediction

**Result: R² 0.777, MAE 0.484 mg/m³** (Random Forest) · Linear Regression R² 0.567.

## The problem
Power plants must continuously prove their emissions stay within limits. Physical analysers are costly; a model that infers CO from ordinary process sensors is called a Predictive Emission Monitoring System (PEMS).

## Data
UCI Gas Turbine CO and NOx Emission Data — 36733 hourly records over 5 years, 9 sensor features.

## Approach
- 75/25 split; Random Forest (200 trees) vs scaled linear baseline

## Run it
Open `gas_turbine_emissions.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

## Stack
Python · pandas · scikit-learn · matplotlib
