# 65 · Car Evaluation Classification

**Result: 97.2% accuracy (Random Forest) · Logistic Regression 93.1% · always predicting the majority class (unacceptable) scores 70.1% on the test set.**

## The problem
1,728 cars, each described by six categorical attributes — buying price, maintenance price, number of doors, persons capacity, luggage-boot size and safety. Predict the overall acceptability: unacceptable, acceptable, good or very good — a deliberately imbalanced, all-categorical problem.

## Data
UCI Car Evaluation (id 19) — 1,728 cars, 6 categorical features, one-hot encoded before training. No missing values.

## Classes
- unacceptable: 1,210 cars
- acceptable: 384 cars
- good: 69 cars
- very good: 65 cars

## Honest note
The headline is flattered by the majority class — 303 of 432 test cars are 'unacceptable' and the forest gets 98% of those right. The rarer 'good' and 'very good' classes (17 and 16 test cars) are still recognised at 94% and 88% recall, so this is not just a majority-class trick, but their small test counts mean those scores should be read with care.

## Approach
- Stratified 75/25 split
- Random Forest (300 trees) vs scaled logistic regression

## Run it
Open `car_evaluation.ipynb` in Jupyter or Colab; it downloads the UCI dataset itself.

![Confusion matrix](confusion_matrix.png)

## Stack
Python · pandas · scikit-learn · matplotlib
