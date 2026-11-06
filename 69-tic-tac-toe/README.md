# 69 · Tic-Tac-Toe Endgame Classification

**Result: 97.9% accuracy (Logistic Regression) · Random Forest 97.5% · always predicting the majority outcome (x won) scores 65.4% on the test set.**

## The problem
958 completed tic-tac-toe boards, each described by the contents of its nine squares (x, o or blank). Predict whether the x player won — a pure logic problem with a known answer, but one that generic classifiers must learn from examples alone.

## Data
UCI Tic-Tac-Toe Endgame (id 101) — 958 boards, 9 categorical features, one-hot encoded before training. No missing values.

## Classes
- positive (x won): 626 boards
- negative (x did not win): 332 boards

## Honest note
Both models are close to the ceiling for learned models here — the game has a deterministic winning rule, so a perfect rule-based solver would score 100%, and these models miss only 5-6 of 240 test boards. The linear model edges the forest by one board, which is noise at this sample size.

## Approach
- Stratified 75/25 split
- Random Forest (300 trees) vs scaled logistic regression

## Run it
Open `tic_tac_toe.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

![Confusion matrix](confusion_matrix.png)

## Stack
Python · pandas · scikit-learn · matplotlib
