# **Neural Network Regression for Housing Price Prediction**

## **Description**
This project leverages a **feedforward neural network (FNN)** to predict housing prices (`MEDV`) using a structured dataset of housing features. The model is implemented using **TensorFlow Keras** and is optimized for regression tasks.

---

## **Dataset**
- The dataset contains various housing features such as crime rate, number of rooms, tax rate, and more.
- Target variable: **MEDV** (Median house value in $1000s).
- Preprocessing includes:
  - **Standardization** of input features using `StandardScaler`.
  - Splitting the data into **training (80%)** and **testing (20%)** subsets.

---

## **Model Architecture**
The neural network has the following structure:
1. **Input Layer**: Matches the number of input features.
2. **Hidden Layer 1**: 64 neurons with **ReLU activation**.
3. **Hidden Layer 2**: 32 neurons with **ReLU activation**.
4. **Output Layer**: Single neuron for regression output.

---

## **Training**
- Optimizer: **Adam** with a learning rate of 0.01.
- Loss function: **Mean Squared Error (MSE)**.
- Metric: **Mean Absolute Error (MAE)**.
- Epochs: **100** with a batch size of **32**.
- 20% of the training data is used for validation.

---

## **Performance Metrics**
1. **Test Loss (MSE)**: Evaluates the average squared difference between actual and predicted values.
2. **R-squared (R²)**: Measures the proportion of variance explained by the model.

### Example Results:
- **Test Loss (MSE)**: `X.XX`
- **Test MAE**: `X.XX`
- **R-squared (R²)**: `X.XX`

---

## **Key Steps**
1. **Preprocessing**:
   - Load and standardize the dataset.
   - Split data into training and testing subsets.

2. **Model Training**:
   - Define the neural network using `Sequential`.
   - Train the model on the scaled training data.

3. **Evaluation**:
   - Assess performance using metrics like MSE and R².
   - Validate the model's performance on unseen test data.

---

## **Visualization**
### 1. **Training and Validation Loss**
- A line plot of **training loss** vs. **validation loss** over epochs to monitor model training and identify overfitting or underfitting.

```python
import matplotlib.pyplot as plt

# Plot training and validation loss
plt.figure(figsize=(8, 6))
plt.plot(history.history['loss'], label='Training Loss')
plt.plot(history.history['val_loss'], label='Validation Loss')
plt.xlabel('Epochs')
plt.ylabel('Mean Squared Error (Loss)')
plt.title('Training and Validation Loss')
plt.legend()
plt.show()
```

---
