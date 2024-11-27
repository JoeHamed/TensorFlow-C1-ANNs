# MNIST Digit Classification with TensorFlow
## Description
This repository contains the implementation of a deep learning model that classifies handwritten digits from the MNIST dataset using TensorFlow. The model is trained until it reaches a specified accuracy threshold (98%) using a custom callback, and then it stops training early. The notebook demonstrates the use of callbacks in TensorFlow, specifically an EarlyStoppingCallback that halts training once the desired accuracy is achieved.

The goal of this assignment was to implement and use callbacks in TensorFlow, optimizing the training process and preventing unnecessary computation.

## Key Concepts
- **MNIST Dataset**: A collection of 28x28 grayscale images of handwritten digits (0-9).
- **Neural Network Architecture**: A feedforward neural network for classification.
- **Early Stopping**: A callback that halts training once a specified accuracy (98%) is reached.
## Code Structure
### 1. Loading and Preprocessing the Data
- The MNIST dataset is loaded from a custom path since it's already included under the data directory.
- The pixel values of the images are normalized from a range of [0, 255] to [0, 1].
### 2. Model Architecture (create_and_compile_model function)
- A simple feedforward neural network is used for digit classification.
- The architecture consists of:
  - A flattening layer to transform the 28x28 image into a 1D array.
  - Dense layers with ReLU activation functions for the hidden layers.
  - A final output layer with 10 units and a softmax activation function to predict the 10 digits (0-9).
### 3. EarlyStoppingCallback (Custom Callback)
A custom callback is implemented that monitors the training process and halts it once the accuracy exceeds 98%.
The on_epoch_end method checks the accuracy after each epoch and stops training if the target accuracy is reached, printing a message indicating that training is being canceled.
4. Training the Model (train_mnist function)
The model is trained on the MNIST dataset using the fit method.
The training stops as soon as the callback detects that the model has reached 98% accuracy.
## Requirements
- Python 3.x
- TensorFlow 2.x
- numpy
