# Logistic Regression for Housing Price Classification

## **Project Description**
This project applies **Logistic Regression** to classify housing prices (`MEDV`) into binary categories based on the **median value** of the dataset. The target variable is transformed into a binary classification problem where values greater than the median are labeled as **1 (High)** and values less than or equal to the median are labeled as **0 (Low)**. The model evaluates its performance on the test dataset and provides metrics such as accuracy and a classification report.

---

## **Algorithm Overview**

### **What is Logistic Regression?**
Logistic Regression is a **supervised machine learning algorithm** used for binary classification tasks. Unlike linear regression, it uses the **sigmoid function** to output probabilities between 0 and 1, which are then converted into binary labels using a threshold (typically 0.5).

### **Steps Performed in this Project**:
1. **Data Loading**: The cleaned housing dataset is loaded.
2. **Feature and Target Separation**:
    - Features (`X`): All columns except `MEDV`.
    - Target (`y`): The median value of `MEDV` is used to create a binary classification target.
3. **Data Preprocessing**:
    - The features are standardized using `StandardScaler` to ensure all features contribute equally to the distance calculations.
4. **Model Training**:
    - A Logistic Regression model is trained on the scaled training data.
5. **Evaluation**:
    - The model's predictions are evaluated using accuracy and a classification report.

---

## **How Logistic Regression Works**
- The model fits a linear equation to the features:
  
  \[ z = w_1x_1 + w_2x_2 + ... + w_nx_n + b \]
  
- Applies the sigmoid function to map the result into probabilities:
  
  \[ \sigma(z) = \frac{1}{1 + e^{-z}} \]
  
- Converts the probabilities to binary outputs based on a threshold (e.g., 0.5).

---

## **Performance Metrics**
1. **Accuracy**: Percentage of correctly classified instances.
2. **Classification Report**:
   - **Precision**: Proportion of true positives among predicted positives.
   - **Recall**: Proportion of true positives among actual positives.
   - **F1-Score**: Harmonic mean of precision and recall.

---

## **Figures and Diagrams**

### **1. Binary Classification Workflow**
```
Features (X) --> Logistic Regression --> Sigmoid Function --> Binary Output (0 or 1)
```

### **2. Sigmoid Function Curve**
The sigmoid function maps values into probabilities between 0 and 1:

\[ \sigma(z) = \frac{1}{1 + e^{-z}} \]

![Sigmoid Curve](https://upload.wikimedia.org/wikipedia/commons/8/88/Logistic-curve.svg)

### **3. Confusion Matrix Representation**
The confusion matrix provides insights into the performance of the model:

| Actual \ Predicted | Low (0) | High (1) |
|---------------------|---------|----------|
| Low (0)            | True Negatives (TN) | False Positives (FP) |
| High (1)           | False Negatives (FN) | True Positives (TP) |



## **Setup and Usage**

1. **Install Required Libraries**:
   ```bash
   pip install pandas scikit-learn matplotlib
   ```

2. **Run the Code**:
   Save the code in a file (e.g., `logistic_regression.py`) and execute it:
   ```bash
   python logistic_regression.py
   ```

3. **Output**:
   - Displays the accuracy and classification report.
   - Prints the confusion matrix and other performance metrics.

---

## **Conclusion**
Logistic Regression is a simple yet effective algorithm for binary classification problems. In this project, it was used to classify housing prices as high or low based on the median value. The model's performance, evaluated through accuracy and classification metrics, highlights its ability to generalize on test data while providing interpretable results. Future improvements can include feature engineering, hyperparameter tuning, or the use of ensemble methods for enhanced performance.

![lr](https://dnycf48t040dh.cloudfront.net/fit-in/840x473/What-is-sklearn-Logistic-Regression.png)