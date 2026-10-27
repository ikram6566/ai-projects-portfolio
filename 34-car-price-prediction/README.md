# 34 · Car Price Prediction

**Result: R² 0.893, MAE $1,962** (Random Forest) · Linear Regression R² 0.883.

## The problem
What is a car worth from its spec sheet alone? Using the classic UCI Automobile dataset (201 cars with prices), predict price from engineering and design attributes.

## Approach
- Categorical attributes (make, body style, fuel system…) one-hot encoded; rows without a price dropped
- Random Forest (300 trees) vs scaled linear baseline

## What the model shows
Engine size, curb weight and horsepower carry most of the price signal — the badge matters less than the hardware.

## Run it
Open `car_price_prediction.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

## Stack
Python · pandas · scikit-learn · matplotlib
