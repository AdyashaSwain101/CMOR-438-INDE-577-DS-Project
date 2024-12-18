# **Supervised Learning**

## **Description**
This project demonstrates the use of **Supervised Learning** techniques to predict target variables based on input features. Supervised learning models are trained on labeled data, making them ideal for solving classification and regression problems.

### **What is Supervised Learning?**
Supervised learning involves learning a function that maps an input to an output based on example input-output pairs. The dataset includes **features (X)** and **target labels (y)**:
- **Features**: Input variables used for prediction.
- **Target**: Output variable we aim to predict.

![Supervised Learning Overview](https://upload.wikimedia.org/wikipedia/commons/1/18/Supervised_learning_sample.svg)

---

## **Dataset**
### **Structure**
1. **Features (X)**: Independent variables that influence the prediction.
2. **Target (y)**: The dependent variable or the output we aim to predict.

Example: For predicting housing prices:
- **Features**: Number of rooms, location, size of the house.
- **Target**: House price.

---

## **Supervised Learning Models**
The project explores the following models:
1. **Linear Regression**: For regression tasks to predict continuous values.
2. **Logistic Regression**: For binary classification.
3. **Decision Trees**: For both regression and classification tasks.
4. **Random Forests**: Ensemble method combining multiple decision trees.
5. **Support Vector Machines (SVM)**: For high-dimensional data classification.

---

## **Workflow**
1. **Data Preprocessing**:
   - Handling missing values.
   - Encoding categorical variables.
   - Standardizing or normalizing features.
2. **Train-Test Split**:
   - Divided the dataset into **training (80%)** and **testing (20%)** subsets.
3. **Model Training**:
   - Trained models using the training set.
4. **Evaluation**:
   - Assessed model performance using metrics such as:
     - **Accuracy** (for classification).
     - **Mean Squared Error (MSE)** (for regression).
     - **R² Score** (for regression).

---

## **Visualization**
### **1. Decision Boundary Visualization (For Classification Tasks)**
This plot shows how the model separates different classes in feature space.

![Decision Boundary](https://upload.wikimedia.org/wikipedia/commons/5/56/SVM_margin.png)


---

### **3. Confusion Matrix (For Classification Tasks)**
A confusion matrix evaluates the performance of classification models by comparing predicted and actual labels.

![Confusion Matrix](https://upload.wikimedia.org/wikipedia/commons/2/26/Confusion_matrix.png)

---

## **Evaluation Metrics**
### **For Regression**:
1. **Mean Squared Error (MSE)**: Measures the average squared error between actual and predicted values.
2. **R² Score**: Proportion of variance explained by the model.

### **For Classification**:
1. **Accuracy**: Fraction of correctly predicted samples.
2. **Precision, Recall, and F1-Score**: Evaluate the balance between true positives and false positives.


```



