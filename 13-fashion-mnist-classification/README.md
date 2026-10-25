# Fashion-MNIST Clothing Classification

A neural network (MLP 784→128→10) that recognises **10 types of clothing** from 28×28 images — the Fashion-MNIST benchmark (60,000 training / 10,000 test images).

## Verified result (executed notebook)
- **MLP: 86.5% test accuracy** (trained on a 20,000-image subset for speed; tested on the full 10,000-image test set)

Classes: T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, Ankle boot.

## Run it
Open `fashion_mnist_classification.ipynb` — it downloads the four IDX files itself (no TensorFlow needed) and runs end to end.
