# K-NN Classification with PCA on Iris Dataset

## Project Overview

This project demonstrates **K-Nearest Neighbors (K-NN) classification** on the classic **Iris dataset**. We explore the dataset, preprocess it, tune the K-NN hyperparameters, and visualize results. Additionally, we apply **Principal Component Analysis (PCA)** to reduce dimensionality and visualize class separation and decision boundaries in 2D.

## Dataset

* **Source:** `sklearn.datasets.load_iris()`
* **Samples:** 150
* **Features (4):**

  * Sepal length (cm)
  * Sepal width (cm)
  * Petal length (cm)
  * Petal width (cm)
* **Classes (3):**

  * 0 💖 Setosa
  * 1 💥 Versicolor
  * 2 🌿 Virginica

## Project Workflow

### 1. Exploratory Data Analysis (EDA)

* Countplot to visualize class distribution
* Boxplots to detect outliers
* Correlation heatmap to analyze relationships between features

### 2. Preprocessing

* Split dataset into **training and testing sets** (80/20)
* **Standardize features** using `StandardScaler` to ensure all features contribute equally for distance calculations

### 3. K-NN Hyperparameter Tuning

* Evaluate K-NN accuracy for **k = 1 to 20** using **5-fold cross-validation**
* Choose the best `k` based on highest cross-validated accuracy

### 4. K-NN Classification (Before PCA)

* Train K-NN classifier on original 4-dimensional features
* Evaluate performance using:

  * Accuracy
  * Classification report (precision, recall, F1-score)
  * Confusion matrix

### 5. Principal Component Analysis (PCA)

* Reduce dimensionality to 2 components while preserving most variance
* Visualize cumulative explained variance to check information retention

### 6. K-NN Classification (After PCA)

* Train K-NN on **2D PCA-transformed data**
* Evaluate performance and compare with baseline model

### 7. Visualization

* 2D PCA scatterplot to show class separation
* Decision boundary plot for K-NN in PCA space
* Color-coded by species:

  * 💖 Setosa
  * 💥 Versicolor
  * 🌿 Virginica

## Results

* **Best K for K-NN:** Determined via cross-validation
* **Accuracy (Before PCA):** ~95–97%
* **Accuracy (After PCA):** Slightly lower but visualization becomes easier
* Confusion matrices confirm excellent class separation for Setosa and good separation for Versicolor and Virginica

## Key Insights

* **K-NN** works well on small, well-separated datasets like Iris.
* **Standardization** is crucial since K-NN is distance-based.
* **PCA** reduces dimensionality for visualization without significant loss of accuracy.
* Decision boundary plots help understand how K-NN classifies new samples.

## Libraries Used

* `numpy`
* `pandas`
* `matplotlib`
* `seaborn`
* `scikit-learn`

## Future Improvements

* Explore **other classifiers** like Logistic Regression, SVM, or Random Forest.
* Apply **PCA with more components** to retain 95–99% variance.
* Use **interactive visualizations** (e.g., Plotly) for decision boundaries.

## Usage

1. Clone the repository:

```bash
git clone https://github.com/yourusername/iris-knn-pca.git
```

2. Install dependencies:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

3. Open the Jupyter Notebook and run cells sequentially.
