# Week 1 Assignment: Housing Prices Prediction with Neural Networks
This project demonstrates how to build and train a simple neural network in TensorFlow to predict house prices based on the number of bedrooms. The relationship between bedrooms and price is defined by a linear formula:

- Base cost: $50,000
- Additional cost per bedroom: $50,000
Thus, a 1-bedroom house costs $100,000, a 2-bedroom house costs $150,000, and so on. The goal is for the neural network to learn this relationship and accurately predict prices for houses with more bedrooms.

## Project Highlights
- Input Features: Number of bedrooms (e.g., 1.0, 2.0, 3.0...).
- Target Labels: House prices (scaled to hundreds of thousands, e.g., 1.0, 1.5, 2.0...).
- Model Architecture: A simple neural network with one dense layer.
- Optimization: Stochastic Gradient Descent (SGD) with Mean Squared Error (MSE) loss.
- Training Data: Six examples (1–6 bedrooms with corresponding prices).
- Prediction: Use the trained model to predict prices for houses, such as a 7-bedroom house.
 
## Files in Repository
### 1. C1W1_Assignment.ipynb
This Jupyter Notebook contains the implementation of the assignment. It is divided into the following exercises:
 #### 1. Create Training Data:
  - Generates numpy arrays for bedrooms (features) and prices (targets).
  - Example:
    ```python
    features = np.array([1.0, 2.0, 3.0, 4.0, 5.0, 6.0], dtype=float)
    targets = np.array([1.0, 1.5, 2.0, 2.5, 3.0, 3.5], dtype=float)
    ```
 #### 2. Define and Compile Model:
  - Builds a Sequential model with:
   - A single Dense layer (1 unit).
   - Input shape of (1,) (one-dimensional input for number of bedrooms).
  - Compiles the model with SGD optimizer and MSE loss function.
 #### 3. Train the Model:
 - Trains the model on the training data for 500 epochs.
 - Monitors the loss during training.
 #### 4. Predict Prices:
 - Uses the trained model to predict the price of a house with 7 bedrooms.
 - Outputs the result in hundreds of thousands of dollars.

## How It Works
#### 1. Scaling the Targets: Prices are scaled to hundreds of thousands to simplify the model's learning process.
#### 2. Simple Architecture: The model uses one dense layer since the relationship is linear.
#### 3. Training Process: The model adjusts its weights and biases during training to minimize the MSE loss.
#### 4. Prediction: After training, the model predicts house prices based on the learned relationship.

## Key Learnings
#### - Building a simple neural network for a linear regression problem.
#### - Using TensorFlow's Sequential API to define and train a model.
#### - Applying basic optimization techniques (SGD with MSE).
#### - Scaling data for improved training efficiency.
