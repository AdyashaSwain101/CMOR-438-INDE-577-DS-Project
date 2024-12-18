# Decision Tree Classifier for Wine Quality Prediction

This project uses a Decision Tree Classifier to predict wine quality based on chemical properties of the wine.

## Overview
The project includes:
- Training a Decision Tree Classifier on a dataset of wine samples.
- Evaluating the model's performance using accuracy and a classification report.
- Visualizing the Decision Tree structure for interpretability.

## Dataset
The dataset (`wine.csv`) contains:
- **Features**: Chemical properties of the wine (e.g., acidity, sugar content).
- **Target**: Wine quality (categorical labels).

Ensure the dataset has a column `quality` as the target variable, and the remaining columns are used as features.

## Requirements
Install the following libraries before running the code:
- `pandas`
- `scikit-learn`
- `matplotlib`

Use the command below to install the dependencies:
```bash
pip install pandas scikit-learn matplotlib
```

## How It Works
1. **Load Data**  
   The dataset is loaded into a pandas DataFrame.

2. **Feature and Target Separation**  
   - `X`: Contains feature columns (chemical properties).
   - `y`: Contains the target column (`quality`).

3. **Data Splitting**  
   The data is split into training (80%) and testing (20%) sets.

4. **Model Training**  
   A Decision Tree Classifier is trained on the training set.

5. **Model Evaluation**  
   The model is evaluated using accuracy and a classification report.

6. **Tree Visualization**  
   The Decision Tree structure is visualized using `plot_tree`.

## Usage
Run the following script:
```python
# Load and preprocess data
data = pd.read_csv('wine.csv')

# Split data into features and target
X = data.drop('quality', axis=1)
y = data['quality']

# Split into training and testing sets
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Train the Decision Tree model
dt_model = DecisionTreeClassifier(random_state=42)
dt_model.fit(X_train, y_train)

# Make predictions
y_pred = dt_model.predict(X_test)

# Evaluate the model
accuracy = accuracy_score(y_test, y_pred)
print(f"Accuracy: {accuracy:.2f}")
print(classification_report(y_test, y_pred))

# Visualize the Decision Tree
plt.figure(figsize=(20, 10))
plot_tree(dt_model, feature_names=X.columns, class_names=dt_model.classes_.astype(str), filled=True, rounded=True)
plt.show()
```

## Outputs
- **Accuracy**: Overall model accuracy on the test set.
- **Classification Report**: Precision, recall, F1-score for each quality label.
- **Decision Tree Visualization**: A detailed diagram showing the tree's splits.

## Notes
- Modify `test_size` and `random_state` in `train_test_split` for different splits.
- Tune hyperparameters of `DecisionTreeClassifier` (e.g., `max_depth`, `min_samples_split`) to improve model performance.
