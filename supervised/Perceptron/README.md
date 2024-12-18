# README: Perceptron Algorithm

---

##  **Title**
**Binary Classification of Housing Prices Using the Perceptron Algorithm**

---

## **Description**
This project implements a **Perceptron Algorithm** to classify houses in the Boston Housing dataset into two categories:
1. Houses with prices **above the median value**.
2. Houses with prices **below the median value**.

The dataset is preprocessed, standardized, and split into training and testing sets. The Perceptron algorithm is then applied to predict whether a house's price falls above or below the median price.

---

## **Dataset**
The dataset used is the **Boston Housing Dataset**, which contains 506 data points with 13 features and a target variable (`MEDV`), representing the median value of owner-occupied homes in $1000s.

### Features:
- `CRIM`: Per capita crime rate by town.
- `ZN`: Proportion of residential land zoned for lots over 25,000 sq. ft.
- `INDUS`: Proportion of non-retail business acres per town.
- `CHAS`: Charles River dummy variable (1 if tract bounds river; 0 otherwise).
- `NOX`: Nitric oxides concentration (parts per 10 million).
- `RM`: Average number of rooms per dwelling.
- `AGE`: Proportion of owner-occupied units built prior to 1940.
- `DIS`: Weighted distances to five Boston employment centers.
- `RAD`: Index of accessibility to radial highways.
- `TAX`: Full-value property tax rate per $10,000.
- `PTRATIO`: Pupil-teacher ratio by town.
- `B`: $$1000(Bk - 0.63)^2$$, where $$Bk$$ is the proportion of Black residents by town.
- `LSTAT`: % lower status of the population.

### Target Variable:
- `MEDV`: Median value of owner-occupied homes in $1000s.

---

## **Algorithm**
The **Perceptron Algorithm** is a linear binary classifier that separates data into two classes using a hyperplane.

### Steps:
1. Convert the target variable (`MEDV`) into a binary classification problem:
   - Class 1: House prices above the median value.
   - Class 0: House prices below or equal to the median value.
2. Standardize features using `StandardScaler` to ensure all features have a mean of 0 and a standard deviation of 1.
3. Train the Perceptron model on the training data.
4. Evaluate the model using accuracy and other performance metrics.

---

## **Results**
### Performance Metrics:
The model's performance can be evaluated using metrics such as accuracy, precision, recall, and F1-score.

### Example Output:
```plaintext
Accuracy: 0.85
Classification Report:
              precision    recall  f1-score   support

           0       0.87      0.84      0.85       100
           1       0.83      0.86      0.84       100

    accuracy                           0.85       200
   macro avg       0.85      0.85      0.85       200
weighted avg       0.85      0.85      0.85       200
```

---

## **Visualization**
### Diagram: Perceptron Decision Boundary
Perceptron Decision Boundary

This diagram shows how the Perceptron separates data points into two classes using a linear decision boundary.
![perceptrons](https://ppl-ai-code-interpreter-files.s3.amazonaws.com/web/direct-files/31097403/8b4c89de-6333-490c-9726-e2f6635b1c9e/0/6105d6cc.png)
The diagram you provided is a Perceptron Decision Boundary Visualization that has been reduced to two dimensions using Principal Component Analysis (PCA). This visualization is highly relevant for understanding how the Perceptron algorithm separates the two classes in the cleaned Boston Housing dataset.
Diagram Details
Title: Perceptron Decision Boundary (PCA Reduced)
Axes:
X-axis: Principal Component 1 (PC1)
Y-axis: Principal Component 2 (PC2)
Background Colors:
The two distinct regions (light blue and brown) represent the decision boundary created by the Perceptron algorithm.
Each region corresponds to one of the two classes (house prices above or below the median value).
Data Points:
The scatter points represent the test data, projected into 2D space using PCA.
Points are colored based on their true class labels, with a black edge to improve visibility.

## **How to Run**
1. Ensure you have Python installed along with the required libraries (`pandas`, `numpy`, `scikit-learn`, and `matplotlib`).
2. Load the cleaned Boston Housing dataset (`cleaned_housing.csv`).
3. Run the provided Python script to preprocess data, train the Perceptron model, and evaluate its performance.

---

## **Dependencies**
Install dependencies using pip:
```bash
pip install pandas numpy scikit-learn matplotlib
```



