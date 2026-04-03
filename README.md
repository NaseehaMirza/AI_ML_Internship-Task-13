# AI_ML_Internship-Task-13
# Task 13: PCA – Dimensionality Reduction

## 📌 Objective

The objective of this task is to apply **Principal Component Analysis (PCA)** on the MNIST dataset to reduce dimensionality while preserving maximum variance, and evaluate its impact on model performance.


## 📂 Dataset

* **Primary Dataset:** MNIST (handwritten digits)
* **Total Features:** 784 (28×28 images flattened)
* **Classes:** 10 (digits 0–9)


## 🛠️ Tools & Technologies

* Python
* Scikit-learn
* NumPy
* Pandas
* Matplotlib


## 🚀 Steps Performed

1. Loaded the MNIST dataset using `sklearn.datasets`
2. Flattened image data into feature vectors
3. Applied **StandardScaler** for feature scaling
4. Applied PCA with different components:

   * 2, 10, 30, 50
5. Calculated **explained variance ratio**
6. Plotted **cumulative explained variance**
7. Transformed dataset into reduced dimensions
8. Trained **Logistic Regression**:

   * On original dataset
   * On PCA-reduced datasets
9. Compared accuracy of all models
10. Visualized data using **2D PCA scatter plot**


## Explained Variance Analysis

* First few components capture limited variance
* Around **30–50 components retain ~90–95% variance**
* Helps in reducing dimensionality significantly without major information loss


## 📉 Accuracy Comparison

| Model                           | Accuracy |
| ------------------------------- | -------- |
| Original Dataset (784 features) | ~97%     |
| PCA (2 components)              | ~60%     |
| PCA (10 components)             | ~85%     |
| PCA (30 components)             | ~93%     |
| PCA (50 components)             | ~95%     |


## 📁 Reduced Dataset

The dataset was reduced using PCA with **50 components**.

* Original shape: `(784 features)`
* Reduced shape: `(50 features)`

### Saved Files:

* `train_pca_50.csv`
* `test_pca_50.csv`

Each file contains:

* PCA-transformed features
* Corresponding labels


## 📌 Key Insights

* PCA reduces dimensionality and computation time
* Accuracy improves as number of components increases
* Optimal balance found around **30–50 components**
* Too much reduction leads to information loss


## 📊 Visualization

* 2D PCA scatter plot shows partial separation of digit classes
* Helps in understanding data distribution in reduced space


## ⚖️ Trade-off

| Fewer Components   | More Components           |
| ------------------ | ------------------------- |
| Faster computation | Higher accuracy           |
| Less memory usage  | More information retained |
| Lower accuracy     | Better predictive performance |
