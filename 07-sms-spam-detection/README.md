# SMS Spam Detection

**What it does:** Classifies a text message as **spam** or **ham**.
**Dataset:** UCI SMS Spam Collection — 5,574 messages (5,572 parsed cleanly).
**Verified result:** Logistic Regression **97.5%** · Naive Bayes **97.4%**. Honest detail: spam recall is 0.812 — the model is conservative (spam precision 1.000); a phishing-style demo message slipped through as ham, and the notebook shows it.
**Files:** `sms_spam_detection.ipynb` · `confusion_matrix.png`
