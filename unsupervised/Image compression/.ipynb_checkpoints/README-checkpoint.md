# Image Processing and SVD Analysis

This project demonstrates the application of Singular Value Decomposition (SVD) for image compression and variance analysis using Python. The script downloads an image from a given URL, performs SVD on its grayscale version, visualizes the variance explained by singular values, and reconstructs the image using different numbers of components.

## Features
- Downloads an image from the provided URL.
- Converts the image to grayscale for computational efficiency.
- Performs Singular Value Decomposition (SVD) on the grayscale image.
- Visualizes the variance explained by the top singular values.
- Reconstructs the image using various numbers of components to demonstrate the effect of compression.

## Requirements
To run the script, ensure you have the following Python packages installed:

- `requests`
- `opencv-python`
- `numpy`
- `matplotlib`
- `seaborn`

You can install the required packages using:
```bash
pip install requests opencv-python numpy matplotlib seaborn
```

## Code Workflow
1. **Import Modules**:
   Necessary libraries like `requests`, `cv2` (OpenCV), `numpy`, `matplotlib.pyplot`, and `seaborn` are imported.

2. **Image Download**:
   - The script fetches the image from the provided URL.
   - Saves it locally as `image.png`.

3. **Image Processing**:
   - Reads the image using OpenCV (`cv2`).
   - Converts the image to grayscale for faster computation.

4. **SVD Computation**:
   - Calculates the Singular Value Decomposition of the grayscale image.
   - Outputs the shapes of the resulting matrices (`U`, `S`, and `V`).

5. **Variance Explained**:
   - Computes the variance explained by each singular value.
   - Plots the variance explained by the top 20 singular values using a bar graph.

6. **Image Reconstruction**:
   - Reconstructs the image using a varying number of components (1, 5, 10, 15, 20, and the full number of components).
   - Displays the reconstructed images alongside the original for comparison.

## How to Run
1. Save the script as `image_svd_analysis.py`.
2. Run the script:
   ```bash
   python image_svd_analysis.py
   ```

## Expected Output
1. **Variance Explained Plot**:
   - A bar graph showing the variance explained by the top 20 singular values.

2. **Image Reconstructions**:
   - The original image and reconstructed images using different numbers of components will be displayed.

## Example Code Snippets
### SVD Computation
```python
# Calculating the SVD
u, s, v = np.linalg.svd(gray_image, full_matrices=False)

# Inspect shapes of the matrices
print(f'u.shape: {u.shape}, s.shape: {s.shape}, v.shape: {v.shape}')
```

### Variance Explained Visualization
```python
var_explained = np.round(s**2 / np.sum(s**2), decimals=6)

sns.barplot(x=list(range(1, 21)), y=var_explained[0:20], color="dodgerblue")
plt.title('Variance Explained Graph')
plt.xlabel('Singular Vector', fontsize=16)
plt.ylabel('Variance Explained', fontsize=16)
plt.tight_layout()
plt.show()
```

### Image Reconstruction
```python
comps = [3648, 1, 5, 10, 15, 20]
plt.figure(figsize=(12, 6))

for i in range(len(comps)):
    low_rank = u[:, :comps[i]] @ np.diag(s[:comps[i]]) @ v[:comps[i], :]
    plt.subplot(2, 3, i+1)
    plt.imshow(low_rank, cmap='gray')
    plt.title(f'n_components = {comps[i]}')
plt.show()
```

## Notes
- Ensure your Python environment has an updated version of OpenSSL to avoid warnings related to `urllib3`.
- If you encounter issues with OpenCV (`cv2`), install or upgrade it using:
  ```bash
  pip install opencv-python
  ```


