# Concrete Compressive Strength Prediction

**Result: R² 0.891, MAE 3.7 MPa** (Random Forest) · Linear Regression R² 0.625.

## The project
Predict the compressive strength of concrete from its recipe — cement, slag, fly ash, water, superplasticizer, coarse/fine aggregate and curing age — using the UCI Concrete dataset (1,030 laboratory mixes, strength measured in MPa).

## Method
1. Load the Excel data file from the UCI archive.
2. Random Forest regressor (300 trees) vs Linear Regression, 75/25 split.
3. The forest wins clearly: curing age and cement interact non-linearly, which a linear model cannot express.

## Honest note
Useful for screening recipes in the lab; nowhere near a substitute for testing real site concrete before certifying a structure.

## Run it
Open `concrete_strength_prediction.ipynb` in Google Colab or locally — it downloads the dataset itself.
