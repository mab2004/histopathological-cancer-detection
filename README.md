# Histopathological Cancer Detection

This repository contains the code for a deep learning project focused on the binary classification of cancer in histopathological images. The goal is to build and compare the performance of two different Convolutional Neural Network (CNN) models.

## Models Implemented

1. **Simple CNN**: A custom-built CNN with three convolutional layers.

2. **VGG16 Transfer Learning**: A model leveraging the powerful, pre-trained VGG16 architecture for feature extraction, with a custom classifier on top.

## Key Findings

The project demonstrates a core principle of deep learning: the importance of data.

In the **initial phase**, models were trained on a small dataset. Both the Simple CNN and the Transfer Learning model showed signs of **overfitting**, with high training accuracy but low and fluctuating validation accuracy. At the end of this phase, the Simple CNN had a test accuracy of **82%**, while the Transfer Learning model had **74%**.

In the **second phase**, the training dataset was expanded significantly. This proved to be a critical step. The Simple CNN's test accuracy **dropped to 70%**, suggesting it was not robust enough to generalize with the new data. In contrast, the Transfer Learning model's test accuracy **improved to 81%**, demonstrating its ability to learn more complex and generalizable features from a larger dataset.

Ultimately, the Transfer Learning approach proved to be the more robust and effective solution for this task.

## Project Structure

The dataset is provided as a `cancer_detection.zip` file. Once unzipped, it contains the following folder structure:

```
cancer_detection/
├── train/
│   ├── 0/  (contains images with no cancer)
│   └── 1/  (contains images with cancer)
└── test/
    ├── 0/  (contains images with no cancer)
    └── 1/  (contains images with cancer)
```

The `notebooks/` directory contains the Jupyter notebook or Colab file with the complete code for data preprocessing, model building, training, and evaluation.

## Libraries Used

* TensorFlow

* Keras

* NumPy

* Matplotlib
