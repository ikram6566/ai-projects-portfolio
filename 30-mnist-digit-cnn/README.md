# Handwritten Digit Recognition with a CNN

**Result: 98.86% accuracy** (small CNN, full 10,000-image MNIST test set).

## The project
MNIST again — but with a convolutional network instead of project 05's MLP (96.2%). Two conv blocks (32 → 64 filters) with max-pooling, then a small dense head; trained 5 epochs on the full 60,000 training images.

## Why it matters
The jump from 96% to ~99% is architectural: convolutions share feature detectors across the image and pooling tolerates shifts, so the model learns *shapes* rather than pixel positions. Same data, same task — the inductive bias is the lesson.

## Run it
Open `mnist_digit_cnn.ipynb` in Google Colab or locally — it downloads MNIST itself. Training takes a few minutes on CPU, seconds on a GPU.
