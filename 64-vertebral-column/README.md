# 64 · Vertebral Column Classification

**Result: 80.8% accuracy (Random Forest and Logistic Regression tied) · always predicting the majority condition (spondylolisthesis) scores 48.7% on the test set.**

## The problem
310 patients, each described by six biomechanical features of the pelvis and spine — pelvic incidence, pelvic tilt, lumbar lordosis angle, sacral slope, pelvic radius and grade of spondylolisthesis. Predict whether the patient is normal, has a disc hernia, or has spondylolisthesis.

## Data
UCI Vertebral Column (id 212), 3-class version — 310 patients, 6 features. No missing values.

## Classes
- Spondylolisthesis: 150 patients
- Normal: 100 patients
- Hernia: 60 patients

## Honest note
The headline is carried by spondylolisthesis, which is recognised at 97% recall, while hernia — only 15 test patients — is recalled at just 53%. With 78 test patients in total, the hernia score is noisy, and the two models tie exactly, so neither approach is clearly better here.

## Approach
- Stratified 75/25 split
- Random Forest (300 trees) vs scaled logistic regression

## Run it
Open `vertebral_column.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

![Confusion matrix](confusion_matrix.png)

## Stack
Python · pandas · scikit-learn · matplotlib
