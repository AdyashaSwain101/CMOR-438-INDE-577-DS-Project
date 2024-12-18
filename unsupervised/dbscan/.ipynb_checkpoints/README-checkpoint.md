---

# **DBSCAN Clustering of Countries Based on Energy Characteristics**

## **Description**
This project uses **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)** to group countries based on their energy characteristics, such as **electricity generation**, **demand**, and **power sector emissions**. DBSCAN is a robust unsupervised clustering algorithm that detects clusters of arbitrary shapes and identifies noise (outliers).

---

## **Dataset**
- **Source**: Preprocessed dataset (`preprocessed.csv`) containing the following:
  - **Category**: Type of energy data (e.g., `Electricity generation`).
  - **Variable**: Specific metrics like `Total Generation`, `Demand`, or `Total Emissions`.
  - **Value**: Numerical data corresponding to the variables for different countries.
  - **Area**: Countries included in the dataset.

### **Preprocessing Steps**
1. Filtered for relevant categories:
   - `Electricity generation`
   - `Electricity demand`
   - `Power sector emissions`
2. Pivoted the dataset:
   - Rows represent **countries**.
   - Columns represent **energy variables** (`Total Generation`, `Demand`, `Total Emissions`).
3. Normalized the data using **StandardScaler** for fair distance calculations.
4. Removed rows with missing values.

---

## **DBSCAN Algorithm**
### **How DBSCAN Works**
1. **Core Points**: Points with at least `min_samples` neighbors within a radius (`eps`).
2. **Border Points**: Points close to core points but not dense enough to be core points.
3. **Noise Points**: Points that do not belong to any cluster.

### **DBSCAN Parameters Used**
- **`eps`**: 0.5 (Maximum distance for two points to be considered neighbors)
- **`min_samples`**: 3 (Minimum points required to form a dense cluster)

---

## **Key Implementation Steps**
1. **Clustering**:
   - Applied DBSCAN to identify clusters and noise points.
   - Added cluster labels to the normalized dataset.
2. **Visualization**:
   - Plotted countries based on `Total Generation` and `Total Emissions`, colored by cluster labels.
   - Annotated the plot with country names for clarity.
3. **Cluster Analysis**:
   - Counted the number of clusters and noise points.
   - Listed the countries in each cluster.

---

## **Results**
- **Number of Clusters**: Example output: `X` clusters
- **Number of Noise Points**: Example output: `Y` noise points
- **Countries in Clusters**: Each cluster contains countries with similar energy characteristics.

---

## **Visualizations**
### 1. **DBSCAN Clustering Results**
- Scatter plot showing clusters of countries based on `Total Generation` and `Total Emissions`.
- Noise points (`Cluster -1`) are shown as outliers.

![DBSCAN Example](https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/DBSCAN-density-data-points.svg/1024px-DBSCAN-density-data-points.svg.png)

---

### 2. **Cluster Analysis with Labels**
- Scatter plot with country labels to identify cluster memberships and noise points.

Example:
![Scatter Plot with Labels](https://miro.medium.com/v2/resize:fit:1200/format:webp/1*wrPKPYsC1sWOMWOnWtYvNQ.png)

---

## **Evaluation Metrics**
1. **Silhouette Score**: Measures the quality of clusters by analyzing intra-cluster cohesion and inter-cluster separation.
   - Example:
     ```python
     silhouette_avg = silhouette_score(df_normalized.iloc[:, :-1], clusters)
     print(f"Silhouette Score: {silhouette_avg:.2f}")
     ```

2. **Cluster Validity**: Evaluate cluster density and separation using **Dunn’s Index** (optional with `dbcv`).

---

## **Usage Instructions**
1. Install required libraries:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn dbcv
   ```
2. Save the preprocessed data file as `preprocessed.csv`.
3. Run the script to cluster the data and visualize results:
   ```bash
   python dbscan_energy_clustering.py
   ```

---
