# CIFAR-10 Image Classification (CNN)

A convolutional neural network that classifies 32×32 colour images into 10 classes — airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck — on the real **CIFAR-10** dataset (60,000 images).

## Verified result (executed notebook)
- **60.0% accuracy** on the full 10,000-image test set
- Small CNN (2 conv blocks + dense head), 8 epochs, trained on a 20,000-image subset

## Run it
Open `cifar10_image_classification.ipynb` — it downloads CIFAR-10 itself and runs end to end. Training takes a few minutes on CPU.

## Honest note
60% is what a compact CNN honestly reaches with this little training; the dataset's state of the art (large models, full 50,000-image training, augmentation) is above 95%. The gap is the lesson: architecture scale, data augmentation and training budget matter more than clever code at this level. Compare Project 13 (MLP on Fashion-MNIST, 86.5%) — grey 28×28 clothing images are simply an easier problem than colour photos of real objects.

## Why it matters
CNNs are the workhorse of computer vision — product-photo tagging, quality inspection, medical imaging and self-driving perception all build on exactly these conv/pool blocks.
