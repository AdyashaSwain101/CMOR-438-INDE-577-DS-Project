# README: Linear Regression on Cleaned Boston Housing Dataset

---

## **Project Title**
**Predicting House Prices Using Linear Regression**

---

## **Description**
This project implements a **Linear Regression** model to predict the median value of owner-occupied homes (`MEDV`) in the Boston Housing dataset. The dataset contains 13 features that describe various socioeconomic and physical attributes of houses in Boston neighborhoods.

Linear Regression is a simple yet powerful algorithm that models the relationship between a dependent variable (target) and one or more independent variables (features). It assumes a linear relationship between the features and the target variable.

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
**Linear Regression** is a supervised learning algorithm used for regression tasks. It fits a straight line (or hyperplane) to minimize the error between predicted and actual values. The model learns coefficients for each feature, which represent their contribution to the target variable.

### Steps:
1. Load and preprocess the cleaned Boston Housing dataset.
2. Split the data into training (80%) and testing (20%) sets.
3. Train a Linear Regression model on the training data.
4. Evaluate the model using performance metrics such as Mean Squared Error (MSE) and R-squared ($$R^2$$).

---

## **Results**
### Performance Metrics:
The model's performance on the test set is evaluated using:
1. **Mean Squared Error (MSE)**: Measures average squared differences between predicted and actual values.
2. **R-squared ($$R^2$$)**: Indicates how well the model explains variance in house prices.

Example Output:
```plaintext
Mean Squared Error: 24.29
R-squared Score: 0.67
```

---

## **Visualization**
### Diagram: Actual vs Predicted Values
The scatter plot below shows how well the predicted house prices match the actual prices:
![LR](https://ppl-ai-code-interpreter-files.s3.amazonaws.com/web/direct-files/31097403/c81a8907-7eed-4486-9e49-dca99c73b810/0/6105d6cc.png)
Actual vs Predicted Values

#### Key Insights:
1. Points close to the diagonal red line indicate accurate predictions.
2. Deviations from the line represent prediction errors.

---

## **How to Run**
1. Ensure you have Python installed along with required libraries (`pandas`, `numpy`, `scikit-learn`, and `matplotlib`).
2. Load the cleaned Boston Housing dataset (`cleaned_housing.csv`).
3. Run the provided Python script to preprocess data, train the Linear Regression model, and evaluate its performance.

---

## **Dependencies**
Install dependencies using pip:
```bash
pip install pandas numpy scikit-learn matplotlib
```

---

