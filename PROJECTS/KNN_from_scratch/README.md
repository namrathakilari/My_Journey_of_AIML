# K-Nearest Neighbors (KNN) From Scratch on Iris Dataset

This project demonstrates an end-to-end implementation of the **K-Nearest Neighbors (KNN)** classification algorithm **from scratch using NumPy**, and compares its performance with **Scikit-learn’s KNeighborsClassifier**.  
It also includes **visualizations** such as **Voronoi diagrams**, **decision boundaries**, **confusion matrices**, and a **classification report** to better understand model behavior.

---

## 📌 Project Overview

- Implement KNN algorithm manually (no ML libraries for core logic)
- Evaluate performance on the **Iris dataset**
- Compare results with Scikit-learn’s implementation
- Visualize:
  - Voronoi diagrams
  - Decision boundaries
  - Confusion matrix
- Generate classification metrics:
  - Accuracy
  - Precision
  - Recall
  - F1-score

---

## 📂 Dataset

- **Iris Dataset** (from `sklearn.datasets`)
- 150 samples
- 4 features:
  - Sepal length
  - Sepal width
  - Petal length
  - Petal width
- 3 target classes:
  - Setosa
  - Versicolor
  - Virginica

---

## ⚙️ Technologies Used

- Python 3
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- SciPy

---

## 🧠 KNN Algorithm (From Scratch)

### Steps:
1. Compute **Euclidean distance** between test point and all training points
2. Sort distances
3. Select the top **K nearest neighbors**
4. Use **majority voting** to assign the class label

### Key Functions:
- `predict()` – predicts label for a single test point
- `k_nearest_neighbor()` – predicts labels for the test set
- `Accuracy()` – computes classification accuracy

---

## 📊 Model Evaluation

### Metrics Used:
- Accuracy
- Confusion Matrix
- Precision
- Recall
- F1-Score

### Comparison:
- Custom KNN implementation
- Scikit-learn `KNeighborsClassifier`

Both implementations yield **comparable accuracy**, validating the correctness of the custom approach.

---

## 📈 Visualizations

### 1. Voronoi Diagram
- Visualizes spatial partitioning of the dataset
- Uses the first two features for 2D representation

### 2. Decision Boundary
- Displays class separation for different KNN weight strategies:
  - `uniform`
  - `distance`

### 3. Confusion Matrix
- Tabular and heatmap representations
- Shows true vs predicted labels

---

## 📑 Classification Report

Includes:
- Precision
- Recall
- F1-score
- Support for each class

Useful for understanding class-wise performance beyond accuracy.

---

# Author
- Namratha Kilari
- namrathakilari37@gmail.com

