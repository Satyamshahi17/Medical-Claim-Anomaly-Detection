# Medical Claims Anomaly Detection

This project explores anomaly detection in synthetic medical claim data using the Isolation Forest algorithm.

## Overview

The goal was to identify unusual or potentially fraudulent claim records without having any labeled data.

- Total Samples: 5,000 (synthetic medical claim data)
- Algorithm Used: Isolation Forest
- Contamination Parameter: `0.01`

## Approach

1. **Initial Attempt without Gaussian Transformation**
   - Raw data was processed and Isolation Forest was applied.
   - A 2D scatter plot was generated to visualize the clusters and outliers.
   - The anomalies detected were not well-separated or interpretable.

2. **Applied Gaussian Transformation**
   - Used `PowerTransformer` to make the data distribution closer to Gaussian.
   - This led to significantly more anomalies being detected (as expected).
   - Helped make the anomaly boundaries more consistent.

3. **Dimensionality Reduction**
   - Applied PCA to reduce the dataset to 3D for better visualization.
   - However, 3D plots didn’t provide meaningful insights or improvements in interpretation.
   - Reverted to using 2D PCA visualization for better clarity.

4. **Visualization**
   - 2D scatter plots were used to observe data structure and anomaly spread.
   - Plotted anomalies vs normal points to understand data behavior post-transformation.

## Key Notes

- The project is fully unsupervised. There are no labels and so no evaluation metrics like precision, recall, or F1 score.
- Focused on trying different preprocessing and visualization techniques to interpret results.
- Anomaly count varied significantly depending on the transformation used.
- Visualization played a key role in understanding the impact of preprocessing.

## Tools Used

- Python
- scikit-learn (IsolationForest, PowerTransformer, PCA)
- matplotlib

