# Movie Recommendation System

A matrix-factorization recommender: it learns hidden "taste factors" for users and movies with SVD, predicts how a user would rate movies they have never seen, and serves a personal top-5 list.

## Data
**MovieTweetings** — real movie ratings shared publicly on Twitter (0–10 scale). The project uses the active-user / popular-movie subset: **413,402 ratings from 3,976 users across 2,982 movies**, so the rating matrix fits in memory.

## Verified result (executed notebook)
- **Test RMSE: 1.51** (on the 0–10 rating scale)
- Mean-rating baseline RMSE: 1.73 — the model cuts prediction error by ~13% versus guessing the average

Example output — top 5 for one user: *X-Men: Days of Future Past* (8.55), *Avengers: Endgame* (8.54), *The Imitation Game* (8.50), *Fury* (8.48), *1917* (8.47).

## Run it
Open `movie_recommendation_system.ipynb` — it downloads the ratings itself and runs end to end.

## Why it matters
This is the core algorithm behind "because you watched…" rows on streaming platforms: no content features, no genres — taste is inferred purely from who liked what.
