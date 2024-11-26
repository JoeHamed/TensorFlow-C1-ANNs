# Week 1 Assignment: Housing Prices Prediction with Neural Networks
This project demonstrates how to build and train a simple neural network in TensorFlow to predict house prices based on the number of bedrooms. The relationship between bedrooms and price is defined by a linear formula:

- Base cost: $50,000
- Additional cost per bedroom: $50,000
Thus, a 1-bedroom house costs $100,000, a 2-bedroom house costs $150,000, and so on. The goal is for the neural network to learn this relationship and accurately predict prices for houses with more bedrooms.

Project Highlights
Input Features: Number of bedrooms (e.g., 1.0, 2.0, 3.0...).
Target Labels: House prices (scaled to hundreds of thousands, e.g., 1.0, 1.5, 2.0...).
Model Architecture: A simple neural network with one dense layer.
Optimization: Stochastic Gradient Descent (SGD) with Mean Squared Error (MSE) loss.
Training Data: Six examples (1–6 bedrooms with corresponding prices).
Prediction: Use the trained model to predict prices for houses, such as a 7-bedroom house.
Files in Repository
1. housing_prices_prediction.ipynb
This Jupyter Notebook contains the implementation of the assignment. It is divided into the following exercises:

