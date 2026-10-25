# Mushroom Classification — Edible or Poisonous?

**Result: 100.0% accuracy, poisonous-class recall 100.0%** (Random Forest, UCI Mushroom dataset, 8,124 specimens).

## The project
Classify mushrooms as edible or poisonous from 22 physical characteristics (cap, gills, stalk, odour, spore print…). This dataset is famously close to perfectly separable — odour alone nearly decides it — so the near-perfect score says as much about the data as the model.

## Method
1. Load from the UCI archive; one-hot encode all characteristics.
2. Random Forest (200 trees), stratified 75/25 split.
3. Report accuracy **and poisonous recall** — the only unforgivable error is calling a poisonous mushroom edible. Confusion matrix saved as `confusion_matrix.png`.

## ⚠️ Safety
A learning exercise on textbook data. **Never eat a wild mushroom based on a model** — real identification needs an expert, and species outside this field-guide dataset are simply absent from it.

## Run it
Open `mushroom_classification.ipynb` in Google Colab or locally — it downloads the dataset itself.
