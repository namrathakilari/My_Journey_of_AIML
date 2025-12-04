# K-NN Classification with PCA on the Iris Dataset

This project demonstrates a complete machine learning workflow using the Iris dataset. It includes **data exploration, preprocessing, K-Nearest Neighbors (K-NN) classification, hyperparameter tuning, dimensionality reduction using PCA, and visualization** of results.  

---

## Project Overview

- **Goal:** Predict Iris species (*setosa, versicolor, virginica*) using K-NN.  
- **Comparison:** Evaluate K-NN performance before and after applying PCA.  
- **Key Steps:**  
  1. Data exploration and visualization  
  2. Preprocessing (train-test split and feature scaling)  
  3. K-NN hyperparameter tuning  
  4. Model training and evaluation  
  5. Dimensionality reduction using PCA  
  6. Model evaluation after PCA  
  7. Visualization of data and decision boundaries  

---

## Dataset

- Source: `sklearn.datasets.load_iris()`  
- Features:  
  - Sepal length (cm)  
  - Sepal width (cm)  
  - Petal length (cm)  
  - Petal width (cm)  
- Target: Iris species (0 = setosa, 1 = versicolor, 2 = virginica)  
- Samples: 150 (50 per class)  

---

## Exploratory Data Analysis (EDA)

- **Class Distribution:** Countplot to visualize number of samples per species  
- **Feature Distribution:** Boxplots to detect outliers  
- **Correlation:** Heatmap to check relationships between features  

---

## Data Preprocessing

- Train-test split: 80/20 with stratified sampling to maintain class balance  
- Feature scaling: StandardScaler to normalize features for distance-based K-NN  

---

## K-NN Hyperparameter Tuning

- Evaluated K values from 1 to 20 using 5-fold cross-validation  
- Plotted K vs. accuracy to select the best K  
- Selected **best_k** based on maximum cross-validated accuracy  

---

## Model Training & Evaluation (Before PCA)

- Trained K-NN with **best_k** on standardized features  
- Metrics:  
  - Accuracy  
  - Classification report (precision, recall, F1-score)  
  - Confusion matrix  

---

## Principal Component Analysis (PCA)

- Reduced feature space from 4D → 2D  
- Plotted cumulative explained variance to assess information retention  
- 2D PCA allows visualizing decision boundaries  

---

## Model Training & Evaluation (After PCA)

- Trained K-NN on PCA-transformed 2D data  
- Evaluated with the same metrics as above  
- Observed slight accuracy decrease due to dimensionality reduction, but gain in interpretability and visualization  

---

## Visualization

- **2D PCA Scatterplot:** Shows class separation in PCA space  
- **Decision Boundary Plot:** Illustrates how K-NN divides the 2D space among classes  
- Color mapping:  
  - Setosa → Green  
  - Versicolor → Red  
  - Virginica → Blue  

---

## Key Takeaways

- K-NN performance is **sensitive to feature scaling**; standardization is essential  
- PCA effectively reduces dimensionality while preserving most of the variance  
- Decision boundaries help visually understand classifier behavior  
- Iris dataset is well-separated, enabling high K-NN accuracy  

---

## Technologies & Libraries

- Python 3.x  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  

---

## How to Run

1. Clone the repository  
2. Install dependencies:  
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```
---

# Author
- Namratha Kilari
- Contact: namrathakilari37@gmail.com
