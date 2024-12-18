# **K-Nearest Neighbors (KNN) Regression for Housing Price Prediction**

## **Description**
This project employs the **K-Nearest Neighbors (KNN) algorithm** to predict housing prices (`MEDV`) based on housing features. KNN calculates predictions using the average of the target values (`MEDV`) of the nearest neighbors determined by a distance metric.

---

## **Dataset**
- **Features**: Housing attributes like `RM` (average number of rooms), `LSTAT` (percentage lower status of population), and `TAX` (property tax rate).
- **Target Variable**: **`MEDV`** (Median home value in $1000s).
- The dataset is preprocessed with:
  - **Feature Scaling**: Using `StandardScaler` for fair distance-based computations.
  - **Train-Test Split**: Dividing data into 80% training and 20% testing subsets.

---

## **Model Overview**
KNN works by:
1. Calculating distances between data points (e.g., Euclidean distance).
2. Identifying the **K closest neighbors** to a test point.
3. Predicting the output as the **mean value of the K neighbors' target values**.

---

## **Steps to Run**
1. Install required libraries:
   ```bash
   pip install pandas numpy scikit-learn matplotlib
   ```
2. Run the code:
   ```bash
   python knn_regression.py
   ```
3. Analyze the results, including metrics such as Mean Squared Error (MSE) and R² Score.

---

## **Visual Explanation of KNN**
### 1. **KNN Conceptual Diagram**
- This image illustrates how the KNN algorithm identifies the nearest neighbors based on the chosen value of `K` and predicts the average.

![KNN Diagram](https://upload.wikimedia.org/wikipedia/commons/e/e7/KnnClassification.svg)

---

### 2. **Actual vs Predicted Values (Visualization Example)**
- A scatter plot that compares the actual and predicted housing prices:
  
![Actual vs Predicted](https://miro.medium.com/max/700/1*q2Ew53vBkiNFuVM67gnfQA.png)

---

### 3. **Error Distribution (Histogram Example)**
- A histogram showing the residuals (errors) in predictions, with a symmetric distribution around zero indicating good model performance:

![Error Distribution](https://res.cloudinary.com/practicaldev/image/fetch/s--PIFRHP9H--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://i.stack.imgur.com/NC4tY.png)

---

## **Evaluation Metrics**
- **Mean Squared Error (MSE)**: Quantifies the average squared error between actual and predicted values.
- **R² Score**: Measures the proportion of variance explained by the model.

---


