# 54 · Image Segmentation Classification

**Result: 96.9% accuracy (Random Forest) · Logistic Regression 93.4% · always predicting any single scene type scores about 14.3% on the test set, since the classes are balanced.**

## The problem
Every instance is a 3x3 region from one of seven outdoor images, described by 19 measurements of colour, edges and texture. Label each region as brickface, sky, foliage, cement, window, path or grass — the pixel-level labelling step behind image understanding.

## Data
UCI Statlog (Image Segmentation) (id 147) — 2,310 regions, 19 features. No missing values. The region-pixel-count feature is constant (9, every region is 3x3) and is dropped.

## Classes
- brickface: 330 regions
- sky: 330 regions
- foliage: 330 regions
- cement: 330 regions
- window: 330 regions
- path: 330 regions
- grass: 330 regions

## Honest note
Unlike most benchmarks in this portfolio, this one is perfectly balanced, so the headline is not flattered by a majority class — 96.9% here means the models really do separate the seven scene types. The remaining errors are concentrated where scene types genuinely look alike in colour and texture.

## Approach
- Stratified 75/25 split
- Random Forest (300 trees) vs scaled logistic regression

## Run it
Open `image_segmentation.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

![Confusion matrix](confusion_matrix.png)

## Stack
Python · pandas · scikit-learn · matplotlib
