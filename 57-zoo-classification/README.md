# 57 · Zoo Animal Type Classification

**Result: 92.3% accuracy (Random Forest and Logistic Regression tied) · always predicting the majority type (mammal) scores 42.3% on the test set.**

## The problem
101 animals, each described by 16 yes/no traits — hair, feathers, eggs, milk, airborne, aquatic, predator, toothed, backbone, breathes, venomous, fins, legs, tail, domestic, catsize — plus a name. Predict the animal's type from its traits alone.

## Data
UCI Zoo (id 111) — 101 animals, 16 features (the animal name is an identifier and is dropped). No missing values.

## Classes
- mammal: 41 animals
- bird: 20 animals
- fish: 13 animals
- reptile: 5 animals
- amphibian: 4 animals
- insect: 8 animals
- invertebrate: 10 animals

## Honest note
The test set has only 26 animals, and the two errors are exactly the two rarest types in it: the single amphibian and the single reptile in the test set are both missed. With one test example each, those per-class scores are meaningless — the headline is carried by mammals and birds, which the models get right.

## Approach
- Stratified 75/25 split
- Random Forest (300 trees) vs scaled logistic regression

## Run it
Open `zoo_classification.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

![Confusion matrix](confusion_matrix.png)

## Stack
Python · pandas · scikit-learn · matplotlib
