# **PCA Analysis of Energy Dataset**

## **Description**
This project performs **Principal Component Analysis (PCA)** on an energy dataset to reduce dimensionality and visualize key patterns in energy-related data across countries. The analysis focuses on features such as **electricity demand**, **generation**, and **power sector emissions**, enabling better understanding of the underlying data structure while retaining maximum variance.

---

## **Dataset Overview**
- **Source**: Preprocessed dataset (`preprocessed.csv`) containing:
  - **Category**: Broad types of data (e.g., `Electricity generation`, `Electricity demand`).
  - **Subcategory**: Subtypes like `Total`, `Demand`, and `CO2 intensity`.
  - **Value**: Numerical data for each feature.
  - **Area**: Country names.
  
### **Preprocessing Steps**
1. Filtered relevant **categories** and **subcategories**:
   - Categories: `Electricity generation`, `Electricity demand`, `Power sector emissions`.
   - Subcategories: `Total`, `Demand`, `CO2 intensity`.
2. Pivoted data:
   - Rows: Countries.
   - Columns: Flattened combinations of categories and subcategories.
3. **Normalization**:
   - Standardized feature values using `StandardScaler` for consistent PCA computations.

---

## **Principal Component Analysis (PCA)**
### **What PCA Does**:
1. Reduces the dataset's dimensions by creating new components.
2. These components are **linear combinations of original features**.
3. Each component explains a portion of the total variance in the data.

### **Key Parameters**:
- **Number of Components**: 2 principal components were retained for visualization.

---

## **Results**
1. **Explained Variance Ratio**:
   - Principal Component 1: `X.XX`
   - Principal Component 2: `Y.YY`
   - **Total Variance Explained**: `Z.ZZ`

2. **Feature Importance**:
   - Feature contributions to **Principal Component 1 (PC1)**.

Example:
| Feature                    | Importance |
|----------------------------|------------|
| `Electricity Demand_Total` | 0.85       |
| `Electricity Generation_Total` | 0.15  |

---

## **Visualizations**
### **1. PCA Concept Illustration**
A visualization showing how PCA reduces dimensionality by projecting data onto principal components.

![PCA Illustration](https://upload.wikimedia.org/wikipedia/commons/e/e4/PCA_illustration.svg)

*(Source: Wikipedia)*

---

### **2. Scatter Plot of Principal Components**
This scatter plot visualizes the countries projected onto the first two principal components.

```python
# Code to create the scatter plot (already provided in the main script)
```

**Example Output**:
![PCA Scatter Plot](https://miro.medium.com/v2/resize:fit:800/format:webp/1*QSPVdDh_FGPc1WwFx6huQg.png)

---

### **3. Explained Variance Plot**
This bar plot illustrates the variance explained by each principal component.

![Explained Variance](https://upload.wikimedia.org/wikipedia/commons/1/1a/Explained_variance_PCA.png)

---

## **Usage Instructions**
### **Dependencies**
- Install required libraries:
   ```bash
   pip install pandas numpy scikit-learn matplotlib
   ```

### **Steps to Run**
1. Place the preprocessed dataset (`preprocessed.csv`) in the appropriate folder.
2. Run the PCA analysis script:
   ```bash
   python pca_analysis.py
   ```
3. Review the visualizations and explained variance metrics.

---

## **Evaluation**
- **Explained Variance Ratio**: Indicates how much information each principal component retains.
- **Feature Importance**: Highlights the most influential variables for PC1.

---
