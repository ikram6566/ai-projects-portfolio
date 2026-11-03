# 53 · Ecoli Protein Localisation Classification

**Result: 88.1% accuracy (Logistic Regression) · Random Forest 86.9% · always predicting the majority class (cp, cytoplasm) scores 42.9% on the test set.**

## The problem
Where does an E. coli protein end up inside the cell? Seven sequence-derived scores predict its localisation site among eight sites. The catch is the same as in the yeast project: the classes are wildly uneven.

## Data
UCI Ecoli (id 39) — 336 proteins, 7 features (the Sequence column is an identifier and is dropped). No missing values.

## Classes
- cp (cytoplasm): 143 proteins
- im (inner membrane): 77 proteins
- pp (periplasm): 52 proteins
- imU (inner membrane, uncleavable signal): 35 proteins
- om (outer membrane): 20 proteins
- omL (outer membrane lipoprotein): 5 proteins
- imS (inner membrane, cleavable signal): 2 proteins
- imL (inner membrane lipoprotein): 2 proteins

## Honest note
This dataset is heavily imbalanced, and the split shows it plainly: imL, with only 2 proteins in the whole dataset, has no proteins at all in the test set, so its per-class score is undefined here, and imS has just one. Both models effectively learn the big classes and mostly miss the rare ones. Read the per-class report and the confusion matrix, not the headline accuracy.

## Approach
- Stratified 75/25 split
- Random Forest (300 trees) vs scaled logistic regression

## Run it
Open `ecoli_classification.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

![Confusion matrix](confusion_matrix.png)

## Stack
Python · pandas · scikit-learn · matplotlib
