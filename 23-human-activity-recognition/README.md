# Human Activity Recognition (Smartphone Sensors)

**Result: 95.5% accuracy** (Logistic Regression) on volunteers the model never saw.

## The project
Recognise 6 activities — walking, walking upstairs, walking downstairs, sitting, standing, laying — from smartphone accelerometer + gyroscope features. UCI HAR dataset: 7,352 training windows and 2,947 test windows, 561 engineered features each, split **by volunteer** so the test measures generalisation to new people.

## Method
1. Load the published feature matrices from the UCI archive (nested zip).
2. Standardise; multinomial Logistic Regression.
3. Evaluate on the held-out volunteers; confusion matrix saved as `confusion_matrix.png` — the residual errors are the physically similar pairs (sitting vs standing).

## What I learned
Good features beat fancy models: with this feature engineering, a linear model is near the ceiling — and split-by-person is the only honest evaluation for wearable data.

## Run it
Open `human_activity_recognition.ipynb` in Google Colab or locally — it downloads the dataset itself.
