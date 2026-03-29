# CNN-Based Handwritten Digit Classification (MNIST)

## Project Overview

This project implements a **Convolutional Neural Network (CNN)** using Keras to classify handwritten digits from the MNIST dataset.
The goal is to design, train, and evaluate a deep learning model while comparing the performance of multiple optimization algorithms.

##  Objectives

* Build a CNN model from scratch following a specified architecture
* Train the model using different optimizers
* Compare performance based on loss and accuracy
* Understand how deep learning models learn image features
##  Dataset
* **Dataset**: MNIST (Handwritten Digits)
* **Classes**: 10 (Digits 0–9)
* **Image Size**: 28 × 28 (Grayscale)
* **Total Samples**: 70,000 images
##  Model Architecture

The CNN model follows this structure:
* Conv2D (64 filters, kernel size 3×3, stride 2, ReLU)
* Conv2D (32 filters, kernel size 2×2, ReLU)
* MaxPooling2D (pool size 2×2)
* Dropout (0.35)
* Flatten
* Dense (256 units, tanh)
* Dropout (0.5)
* Dense (10 units, softmax)
## Training Configuration

* **Loss Function**: Categorical Crossentropy
* **Epochs**: 10
* **Batch Size**: 32
* **Evaluation Metric**: Accuracy
### Optimizers Compared:

* Adam
* Adadelta
* Stochastic Gradient Descent (SGD)

## Results & Analysis for test dataset

| Optimizer | Accuracy          | Loss       | Observation                              |
| --------- | ----------------- | ---------- | ---------------------------------------- |
| Adam      | 0.9904       | 0.0354  | Best overall performance; fastest convergence and highest accuracy (~99%) |
| Adadelta  | 0.8745            | 0.4939   | Stable but slower and lower accuracy (~87.5%)         |
| SGD       | 0.9861 | 0.0414 | Slightly slower convergence but still high accuracy (~98.6%)     |

### Key Insights:

* Adam achieved the best performance with the lowest validation loss

##  Visualizations

The following plots were generated:

* Training vs Validation Loss
* Training vs Validation Accuracy
* Optimizer Comparison Graphs
## Key Learnings
* Understanding CNN architecture and feature extraction
* Importance of optimizer selection
* Role of dropout in preventing overfitting
* Difference between one-hot and sparse labels
* Proper evaluation using validation and test datasets
##  Conclusion
This project demonstrates the effectiveness of CNNs in image classification tasks.
Through optimizer comparison, it is evident that **Adam provides the best generalization performance** for this architecture.
## Author
Ephrem Ftye
Aspiring Data Scientist

