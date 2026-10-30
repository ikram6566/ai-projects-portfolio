# AI Projects Portfolio 🤖

Forty-five working machine-learning projects, built from scratch and documented end-to-end — data cleaning, model training, honest evaluation, and what I learned from each. Every notebook is self-contained: it downloads its own dataset, so you can run any of them in Google Colab in one click-through.

| # | Project | Type | Result |
|---|---|---|---|
| 1 | [Titanic Survival Prediction](01-titanic-survival/) | Classification | **81.6% accuracy** (Random Forest) |
| 2 | [House Price Prediction](02-house-price-prediction/) | Regression | **R² 0.809, MAE $32,181** (Random Forest) |
| 3 | [Sentiment Analysis](03-sentiment-analysis/) | NLP | **89.9% accuracy** on IMDb 50,000 reviews (TF-IDF + Logistic Regression) |
| 4 | [Fake News Detection](04-fake-news-detection/) | NLP | **97.9% accuracy** on 32,470 full articles (LIAR short-statement version: 60.9% — wording is not proof) |
| 5 | [Handwritten Digit Recognition (MNIST)](05-mnist-digit-recognition/) | Deep Learning | **96.16% accuracy** (Neural Network, 10,000-image test set) |
| 6 | [Iris Flower Classification](06-iris-classification/) | Classification | **94.7% accuracy** (Logistic Regression) |
| 7 | [SMS Spam Detection](07-sms-spam-detection/) | NLP | **97.5% accuracy** (Logistic Regression) |
| 8 | [Breast Cancer Classification](08-breast-cancer-classification/) | Classification | **98.6% accuracy** (Logistic Regression) |
| 9 | [Wine Quality Prediction](09-wine-quality-prediction/) | Classification | **94.0% accuracy** (Random Forest) |
| 10 | [Heart Disease Prediction](10-heart-disease-prediction/) | Classification | **86.8% accuracy** (Logistic Regression + Random Forest) |
| 11 | [Diabetes Prediction](11-diabetes-prediction/) | Classification | **75.5% accuracy** (Random Forest, Pima dataset) |
| 12 | [Customer Churn Prediction](12-customer-churn-prediction/) | Classification | **80.8% accuracy** (Logistic Regression, Telco dataset) |
| 13 | [Fashion-MNIST Clothing Classification](13-fashion-mnist-classification/) | Deep Learning | **86.5% accuracy** (Neural Network, 10,000-image test set) |
| 14 | [Loan Credit-Risk Prediction](14-loan-credit-risk/) | Classification | **72.8% accuracy** (Random Forest, German Credit dataset) |
| 15 | [Rule-Based Chatbot](15-rule-based-chatbot/) | NLP / Rules | **9/9 intent checks passed** (regex intent engine) |
| 16 | [Bank Marketing Prediction](16-bank-marketing-prediction/) | Classification | **90.8% accuracy** (Random Forest, UCI Bank Marketing, 45,211 clients) |
| 17 | [Movie Recommendation System](17-movie-recommendation-system/) | Recommender | **RMSE 1.51 vs 1.73 baseline** (SVD, 413,402 real ratings, 0–10 scale) |
| 18 | [Stock Price Prediction](18-stock-price-prediction/) | Time Series | Honest result: **models did not beat the naive baseline** (MAE $3.07 vs $3.04, AAPL 10 yrs) — random-walk reality check |
| 19 | [CIFAR-10 Image Classification](19-cifar10-image-classification/) | Deep Learning | **60.0% accuracy** (CNN, full 10,000-image test set) |
| 20 | [News Topic Classification](20-news-topic-classification/) | NLP | **92.0% accuracy** (TF-IDF + Logistic Regression, AG News 120,000 articles) |
| 21 | [Credit Card Fraud Detection](21-credit-card-fraud-detection/) | Classification / Imbalanced | **PR-AUC 0.70, fraud recall 88.6%** (284,807 transactions, 0.17% fraud — accuracy deliberately not the headline) |
| 22 | [Census Income Prediction](22-census-income-prediction/) | Classification | **84.7% accuracy** (Logistic Regression; Random Forest 84.3%, UCI Adult, 30,162 records) |
| 23 | [Human Activity Recognition](23-human-activity-recognition/) | Classification / Sensors | **95.5% accuracy** (Logistic Regression, UCI HAR, tested on unseen volunteers) |
| 24 | [Mushroom Classification](24-mushroom-classification/) | Classification | **100% accuracy, 100% poisonous recall** (UCI Mushroom, 8,124 specimens — near-separable dataset, stated plainly) |
| 25 | [Bike Sharing Demand](25-bike-sharing-demand/) | Regression | **R² 0.918, MAE 33 bikes/hour** (Random Forest, UCI Bike Sharing, 17,379 hours) |
| 26 | [Online Shoppers Intention](26-online-shoppers-intention/) | Classification / E-commerce | **89.9% accuracy** (Random Forest; buyer recall 53.2%, UCI Online Shoppers, 12,330 sessions) |
| 27 | [Concrete Strength Prediction](27-concrete-strength-prediction/) | Regression | **R² 0.891, MAE 3.7 MPa** (Random Forest, UCI Concrete, 1,030 mixes) |
| 28 | [Parkinson's Detection](28-parkinsons-detection/) | Classification / Health | **93.9% accuracy** (Logistic Regression, voice measurements — small-n caveat in README) |
| 29 | [20 Newsgroups Classification](29-newsgroups-classification/) | NLP | **82.6% accuracy** (TF-IDF + Logistic Regression, 20 topics, 18,846 posts) |
| 30 | [MNIST Digit CNN](30-mnist-digit-cnn/) | Deep Learning / CV | **98.86% accuracy** (small CNN — vs 96.2% for the MLP in project 05, same data) |
| 31 | [Airfoil Noise Prediction](31-airfoil-noise-prediction/) | Regression | **R² 0.932, MAE 1.32 dB** (Random Forest, NASA airfoil wind-tunnel data, 1,503 runs) |
| 32 | [Energy Efficiency Prediction](32-energy-efficiency-prediction/) | Regression | **R² 0.998, MAE 0.33** (Random Forest, heating load of 768 simulated buildings) |
| 33 | [Beijing PM2.5 Prediction](33-beijing-pm25-prediction/) | Regression | **R² 0.840, MAE 22.3 µg/m³** (Random Forest, 41,757 hourly weather/pollution records) |
| 34 | [Car Price Prediction](34-car-price-prediction/) | Regression | **R² 0.893, MAE $1,962** (Random Forest, UCI Automobile, 201 cars) |
| 35 | [Dry Bean Classification](35-dry-bean-classification/) | Classification | **92.4% accuracy** (Logistic Regression; Random Forest 92.0%, 7 bean varieties, 13,611 beans) |
| 36 | [Forest Cover Type Classification](36-forest-cover-type/) | Classification | **90.8% accuracy** (Random Forest; Logistic Regression 72.4%, UCI Covertype, 581,012 patches, 7 cover types) |
| 37 | [Steel Plate Fault Classification](37-steel-plates-faults/) | Classification / Industrial QC | **79.6% accuracy** (Random Forest; Logistic Regression 72.2%, UCI Steel Plates Faults, 1,941 plates, 7 fault types) |
| 38 | [Abalone Age Prediction](38-abalone-age-prediction/) | Regression | **R² 0.537, MAE 1.55 rings** (Random Forest; Linear Regression R² 0.546 — a famously hard dataset, UCI Abalone, 4,177 specimens) |
| 39 | [Gas Turbine CO Emission Prediction](39-gas-turbine-emissions/) | Regression | **R² 0.777, MAE 0.484 mg/m³** (Random Forest; Linear Regression R² 0.567, UCI Gas Turbine, 36,733 hourly records) |
| 40 | [Letter Recognition](40-letter-recognition/) | Classification / OCR | **97.0% accuracy** (Random Forest, 26 letters; Logistic Regression 77.1%, UCI Letter Recognition, 20,000 letters) |
| 41 | [Superconductor Temperature Prediction](41-superconductor-temperature/) | Regression | **R² 0.925, MAE 5.18 K** (Random Forest; Linear Regression R² 0.728, UCI Superconductivity, 21,263 materials, 81 features) |
| 42 | [Ionosphere Radar Classification](42-ionosphere-radar/) | Classification | **93.2% accuracy** (Random Forest; Logistic Regression 89.8%, UCI Ionosphere, 351 radar returns) |
| 43 | [Glass Type Identification](43-glass-type-identification/) | Classification | **83.3% accuracy** (Random Forest; Logistic Regression 70.4%, UCI Glass, 214 samples, 6 of 7 classes present) |
| 44 | [Online News Popularity Prediction](44-online-news-popularity/) | Regression | **R² 0.158 on log(shares), MAE 2,355 shares** (Random Forest, UCI Online News Popularity, 39,644 articles — an honestly weak-signal problem, stated plainly) |
| 45 | [Waveform Classification](45-waveform-classification/) | Classification | **86.8% accuracy** (Logistic Regression; Random Forest 84.8%, UCI Waveform, 5,000 samples — near the known ~86% Bayes rate) |

## Skills demonstrated
- **Data work:** cleaning, missing values, feature engineering, one-hot encoding (pandas)
- **Classic ML:** Logistic Regression, Random Forest — classification & regression (scikit-learn)
- **NLP:** TF-IDF vectorization, text classification, honest error analysis
- **Neural networks:** MLP image classification on MNIST; CNN image classification on CIFAR-10 (TensorFlow/Keras)
- **Recommenders & time series:** matrix factorization (SVD), chronological splits, return targets, naive-baseline benchmarking
- **Imbalanced & sensor data:** PR-AUC and recall-first evaluation for rare events (fraud), class weighting, split-by-person evaluation for wearable sensor data
- **Applied domains:** e-commerce session behaviour, materials-strength regression, voice-biomarker classification with explicit small-sample caveats, and a CNN-vs-MLP architecture comparison on identical data
- **Physical & environmental data:** aeroacoustics (NASA wind tunnel), building energy simulation, air-quality nowcasting from weather, and honest split-method caveats (random vs time-based)
- **Large & industrial tabular data:** 581k-row forest-cover classification, steel-mill fault diagnosis, predictive emission monitoring (PEMS), and classic OCR feature engineering across 26 classes
- **Materials & signal data:** superconductivity critical-temperature regression, radar-return classification, glass identification on a tiny dataset, social-media popularity prediction with an honestly weak signal, and waveform classification at the theoretical Bayes limit
- **Evaluation discipline:** held-out test sets, confusion matrices, MAE/RMSE/R², no cherry-picked demos — including publishing the project whose models lost to the baseline

## Tools
Python · pandas · NumPy · scikit-learn · matplotlib · Jupyter / Google Colab

## About me
I'm **Ikram ur Rehman** — BS Computer Science (COMSATS), 3+ years as a Marketing Professional & Technical Expert (SEO, Meta/Google Ads, CRM & data, websites, IT support). I build practical AI and automation on top of that foundation. More on my [profile](https://github.com/ikram6566).

*Project ideas selected from my curated [500+ AI Projects with Code](https://github.com/ikram6566/500-AI-Projects-with-Code) collection (Data-Flair beginner lists); all code here is my own build.*
