# Fake News Detection — 32,470 Full Articles

**What it does:** Reads a full news article (headline + body) and predicts **REAL** or **FAKE**.

**Dataset (BIG):** ISOT-style fake/real news collection — **32,470 full-length articles** (24,353 train / 8,117 test; median article ≈ 2,200 characters). Real = Reuters wire stories; fake = sites flagged by fact-checkers.

**Approach:** TF-IDF over headline + body (50,000 unigram+bigram features) → Logistic Regression.

**Verified result (executed notebook):**
- **Accuracy: 97.9%** on 8,117 unseen test articles (FAKE precision 0.976 / REAL precision 0.982)
- Demo on the first 8 test articles (not cherry-picked): **7 of 8 correct**

> **Honest caveats:** (1) This dataset is easier than the real world — real articles are all Reuters copy with a distinctive style, so the model partly learns that style. On the harder LIAR dataset (single short political statements) the same approach scored only **60.9%**. (2) Wording is not proof — a classifier flags suspicious style; only fact-checking verifies a claim. Use it as triage, not as a judge.

![Confusion matrix](confusion_matrix.png)

**Files:** `fake_news_detection.ipynb` — notebook with outputs · `confusion_matrix.png`
**Run it:** Open the notebook in Google Colab or Jupyter — it downloads the dataset itself.
