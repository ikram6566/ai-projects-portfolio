# News Topic Classification (AG News)

Classifies news articles into four topics — **World, Sports, Business, Sci/Tech** — using TF-IDF features + logistic regression on the **AG News** corpus (120,000 training articles, 7,600 test articles).

## Verified result (executed notebook)
- **92.0% accuracy** on the held-out test set
- Sanity check: 4/4 hand-written sample headlines sorted into the right topic

## Run it
Open `news_topic_classification.ipynb` — it downloads the dataset itself and runs end to end.

## Why it matters
Topic classification is the engine behind news tagging, content routing, media monitoring and trend alerts: before you can summarise, recommend or react to an article, a system first has to know what it is about. This project shows a classical TF-IDF pipeline still does that job fast, cheaply and transparently.
