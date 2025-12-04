# Wine Dataset Dimensionality Reduction and Classification

This project explores dimensionality reduction techniques and K-Nearest Neighbors (K-NN) classification on the **Wine dataset**. The goal is to visualize and understand the structure of the data, compare different techniques, and evaluate classification performance.

---

## Project Overview

The Wine dataset consists of 178 samples with 13 features, classified into 3 distinct wine types. The project performs the following steps:

1. **Data Exploration & Preprocessing**
   - Visualize class distribution using count plots.
   - Detect outliers using feature-wise boxplots.
   - Examine feature correlations with a heatmap.
   - Standardize features using `StandardScaler`.

2. **Classification with K-NN**
   - Hyperparameter tuning to select the best `k`.
   - Evaluate performance on the original 13-dimensional dataset.
   - Plot confusion matrix to visualize misclassifications.

3. **Dimensionality Reduction**
   - **PCA (Principal Component Analysis)**
     - Reduce 13 features to 2 components.
     - Visualize variance explained and class separation.
   - **t-SNE (t-distributed Stochastic Neighbor Embedding)**
     - Reduce high-dimensional data to 2D.
     - Experiment with different perplexities (10, 20, 30).
     - Visualize local cluster structure.
   - **UMAP (Uniform Manifold Approximation and Projection)**
     - Reduce data to 2D while preserving local and global structure.
     - Experiment with `n_neighbors` (5, 15, 30) to balance local vs global relationships.
     - Annotate cluster centers for clarity.

4. **Visualization**
   - 2D scatter plots of PCA, t-SNE, and UMAP projections.
   - Decision boundary plots for K-NN on PCA-reduced data.
   - Annotated cluster centers for t-SNE and UMAP visualizations.

---

## Key Findings

- **PCA** provides a quick linear reduction but cannot capture non-linear cluster structure.
- **t-SNE** separates local clusters effectively, especially with smaller perplexities.
- **UMAP** balances local and global structures, with `n_neighbors` controlling the trade-off.
- K-NN classification achieves good accuracy both before and after PCA, but visualizations help understand the separability of classes.

---

## How to Run

1. Clone the repository:

```bash
git clone https://github.com/yourusername/wine-dim-reduction.git
cd wine-dim-reduction
```

2. Install dependencies:
   
```bash
pip install -r requirements.txt
```

3. Run the Jupyter notebook:
   
```bash
jupyter notebook Wine_Dimensionality_Reduction.ipynb
```
# Author
- Namratha Kilari
- namrathakilari37@gmail.com
