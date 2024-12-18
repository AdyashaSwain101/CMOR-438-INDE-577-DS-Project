# **K-Means Clustering of Countries Based on Energy Characteristics**

## **Description**
This project implements **K-Means Clustering** to group countries based on their energy characteristics, such as **electricity generation**, **electricity demand**, and **power sector emissions**. Using the preprocessed dataset, the clustering algorithm identifies patterns and similarities between countries, helping to uncover meaningful insights.

---

## **Dataset Overview**
- **Source**: Preprocessed dataset (`preprocessed.csv`) containing:
  - **Category**: Type of energy data (e.g., `Electricity generation`).
  - **Variable**: Specific metrics like `Total Generation`, `Demand`, or `Total Emissions`.
  - **Value**: Numerical data for each country.
  - **Area**: Names of countries.

### **Preprocessing Steps**
1. **Filter Data**:
   - Included relevant categories: `Electricity generation`, `Electricity demand`, and `Power sector emissions`.
   - Selected key variables: `Total Generation`, `Demand`, and `Total Emissions`.
2. **Pivot Table**:
   - Rows represent countries, and columns represent energy-related variables.
3. **Normalization**:
   - Standardized features using `StandardScaler` to ensure equal importance across variables.

---

## **K-Means Algorithm**
### **How K-Means Works**
1. **Initialization**: Define the number of clusters (`k`) and initialize cluster centroids.
2. **Assignment**: Assign each data point to the nearest cluster centroid.
3. **Update**: Recalculate centroids based on the mean of assigned points.
4. **Repeat**: Iterate until centroids stabilize or a maximum number of iterations is reached.

### **Key Parameters**
- **`n_clusters`**: Number of clusters (e.g., 5).
- **`random_state`**: Ensures reproducibility.

### **Illustration of K-Means**:
![K-Means Illustration](https://upload.wikimedia.org/wikipedia/commons/thumb/e/ea/K-means_convergence.gif/250px-K-means_convergence.gif)

*(Source: Wikipedia)*

---

## **Results**
1. **Number of Clusters**: The dataset was clustered into 5 groups (or more, depending on experimentation).
2. **Cluster Centers**: Identified average energy characteristics for each cluster.
3. **Country Membership**: Countries were assigned to clusters based on their similarity.

### Example Output:
- Cluster Centers:
  ```
  Cluster 0: Avg Generation = X, Avg Demand = Y, Avg Emissions = Z
  Cluster 1: Avg Generation = A, Avg Demand = B, Avg Emissions = C
  ...
  ```
- Countries in Clusters:
  ```
  Cluster 0: Country A, Country B
  Cluster 1: Country C, Country D
  ...
  ```

---

## **Visualizations**
### **1. Scatter Plot of Clusters**
- Shows countries grouped into clusters based on `Total Generation` and `Total Emissions`.

![Cluster Scatter Plot](https://miro.medium.com/v2/resize:fit:800/format:webp/1*fa2hyXY5OOUZrp_dcnCqYA.png)

---

### **2. Elbow Method**
- Visualizes the **inertia** to determine the optimal number of clusters.

![Elbow Method](https://upload.wikimedia.org/wikipedia/commons/thumb/2/28/K-means_convergence.gif/300px-K-means_convergence.gif)

---

### **3. Silhouette, CH, and DB Scores**
- Compare clustering performance across different metrics:
  - **Silhouette Score**: Measures cohesion and separation.
  - **Calinski-Harabasz (CH) Score**: Evaluates cluster density and separation.
  - **Davies-Bouldin (DB) Score**: Lower values indicate better clustering.

---

## **Evaluation**
1. **Silhouette Score**: Measures how well each point fits its assigned cluster.
   - Best Score: `X.XX`
2. **Calinski-Harabasz Score**: Measures the ratio of cluster separation to within-cluster cohesion.
   - Best Score: `Y.YY`
3. **Davies-Bouldin Score**: Lower values indicate more distinct clusters.
   - Best Score: `Z.ZZ`

---

## **Usage Instructions**
### **Dependencies**
- Install required libraries:
  ```bash
  pip install pandas numpy scikit-learn matplotlib
  ```

### **Steps to Run**
1. Place the preprocessed dataset (`preprocessed.csv`) in the `data` folder.
2. Run the script to apply K-Means and visualize clusters:
   ```bash
   python kmeans_clustering.py
   ```

---
