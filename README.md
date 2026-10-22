# EMNIST Character Recognition: MLP vs. CNN

## Overview

This project explores neural-network approaches to handwritten character classification using the **EMNIST Balanced** dataset. It compares a Multilayer Perceptron (MLP) with a series of Convolutional Neural Network (CNN) architectures implemented in PyTorch.

The project focuses on understanding how architecture choices and training techniques affect classification performance.

## Dataset

- **Dataset:** EMNIST Balanced
- **Training samples:** 112,800
- **Test samples:** 18,800
- **Number of classes:** 47
- **Image size:** 28 × 28 pixels
- **Image format:** grayscale

The dataset is downloaded automatically by the notebooks using `torchvision.datasets.EMNIST`.

## Experiments

### 1. Multilayer Perceptron (MLP)

The MLP experiments investigate how network size, batch normalization, dropout, and optimizer settings affect performance.

Notebook: [`emnist_mlp_experiments.ipynb`](notebooks/emnist_mlp_experiments.ipynb)

### 2. Convolutional Neural Networks (CNNs)

The CNN experiments progressively test:

- Number of convolutional layers and channels
- Padding and max pooling
- Batch normalization
- Dropout
- Learning rates and learning-rate scheduling
- Data augmentation
- Global Average Pooling
- Multi-layer convolutional blocks

Notebook: [`emnist_cnn_experiments.ipynb`](notebooks/emnist_cnn_experiments.ipynb)

## Results

Best results observed in the original experiment runs:

| Model | Best observed test accuracy |
|---|---:|
| MLP | 87.27% |
| CNN | 89.85% |

The best observed CNN result came from a two-block convolutional architecture using 32 and 64 channels, batch normalization, max pooling, and dropout.

These results are observations from individual runs, not guaranteed outcomes. Random initialization, data order, and hardware can affect reproduced results.

## Technologies

- Python
- PyTorch
- Torchvision
- NumPy
- Matplotlib
- Pandas

## How to Run

1. Clone or download this repository.
2. Install the dependencies listed in `requirements.txt`.
3. Open either notebook in Jupyter Notebook or Visual Studio Code.
4. Run the cells from top to bottom.

The EMNIST dataset is downloaded automatically when the notebooks are run.

## Purpose

This project demonstrates hands-on experimentation with neural-network architectures, model evaluation, and training techniques for image classification.
