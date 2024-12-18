# Ensemble Learning for Housing Price Prediction

## **Project Description**
This project utilizes **ensemble learning** techniques to predict housing prices (`MEDV`) by combining multiple base models using a **Voting Regressor**. The ensemble includes three models: **Random Forest Regressor**, **Gradient Boosting Regressor**, and **Linear Regression**, leveraging their individual strengths to improve predictive performance. The model is trained on a cleaned housing dataset, and its performance is evaluated using metrics like Mean Squared Error (MSE) and R-squared (R²).

---

## **Algorithm Overview**

### **What is Ensemble Learning?**
Ensemble learning combines predictions from multiple models to achieve better performance than any single model. A **Voting Regressor** aggregates the outputs of base regressors by averaging their predictions.

### **Base Models Used**:
1. **Random Forest Regressor**:
   - A tree-based ensemble model using bagging.
   - Handles non-linear relationships effectively.
2. **Gradient Boosting Regressor**:
   - Sequentially builds models to correct errors from previous ones.
   - Focuses on minimizing residuals.
3. **Linear Regression**:
   - Captures linear relationships between features and the target.

### **Voting Regressor**:
- Combines predictions from all three models by averaging their outputs to provide the final prediction.

---

## **How Ensemble Learning Works**
1. Each base model (`rf`, `gb`, `lr`) is trained independently on the training data.
2. The Voting Regressor aggregates their predictions:
   
   \[
   \hat{y} = \frac{1}{n} \sum_{i=1}^{n} \hat{y}_i
   \]
   
   where \( \hat{y}_i \) is the prediction of the \(i^{th}\) model.
3. The ensemble model outputs the final prediction.

---

## **Performance Metrics**
1. **Mean Squared Error (MSE)**: Measures the average squared difference between predicted and actual values.
2. **R-squared (R²)**: Indicates the proportion of variance in the target variable explained by the model.

---

## **Figures and Diagrams**

### **1. Ensemble Learning Workflow**
```
Features (X) --> Base Models (RF, GB, LR) --> Predictions --> Averaging --> Final Prediction (MEDV)
```

### **2. Comparison of Base Models and Ensemble Performance**
A bar chart can be used to compare MSE and R² values for individual models and the ensemble.

---

## **Setup and Usage**

1. **Install Required Libraries**:
   ```bash
   pip install pandas scikit-learn matplotlib
   ```

2. **Run the Code**:
   Save the code in a file (e.g., `ensemble_learning.py`) and execute it:
   ```bash
   python ensemble_learning.py
   ```

3. **Output**:
   - Displays the ensemble model's MSE and R².
   - Optionally, compare individual base models' performance.

---

## **Conclusion**
Ensemble learning with a Voting Regressor effectively combines the strengths of **Random Forest**, **Gradient Boosting**, and **Linear Regression** to improve predictive performance. The ensemble model benefits from reduced variance (Random Forest), reduced bias (Gradient Boosting), and interpretable linear relationships (Linear Regression). This approach demonstrates robust and accurate predictions for housing prices (`MEDV`). Further improvements can include hyperparameter tuning or adding additional base models for enhanced results.

