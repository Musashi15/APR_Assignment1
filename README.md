# APR_Assignment1
# SVM Classification on Breast Cancer Wisconsin Dataset

## Project Overview
This project demonstrates the implementation of a **Support Vector Machine (SVM)** algorithm for a binary classification task.  
The goal is to classify breast cancer tumors as either **malignant** or **benign** based on diagnostic measurements from digitized images of a fine needle aspirate (FNA).

---

## Dataset
The project uses the **Breast Cancer Wisconsin (Diagnostic) Database**, a classic dataset from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)), conveniently available through **scikit-learn**.

- **Features**: 30 real-valued attributes computed from digitized images describing characteristics of the cell nuclei.  
- **Target Variable**: Binary diagnosis:
  - `Malignant` (harmful)  
  - `Benign` (not harmful)

### Key Features
- `radius_mean`  
- `texture_mean`  
- `perimeter_mean`  
- `area_mean`  
- `smoothness_mean`  
- `compactness_mean`

---

## Methodology
The analysis is conducted in the Jupyter Notebook **`breast_cancer_svm.ipynb`** and follows these steps:

### 1. Data Loading & Exploration
- Load dataset directly from scikit-learn.  
- Perform initial exploratory data analysis (EDA) to understand structure, summary statistics, and class distribution.

### 2. Data Preprocessing
- Separate features (`X`) and target variable (`y`).  
- Split data into **80% training** and **20% testing**, using stratification to preserve class balance.  
- Standardize features with `StandardScaler` (important for SVM performance).

### 3. Model Training
- Instantiate a **Support Vector Classifier (SVC)** with a **linear kernel**.  
- Train the model on preprocessed training data.

### 4. Model Evaluation
- Evaluate on test set using:
  - **Accuracy Score**: Overall prediction correctness.  
  - **Confusion Matrix**: True/false positives & negatives.  
  - **Classification Report**: Precision, recall, F1-score per class.

### 5. Visualization
- Apply **Principal Component Analysis (PCA)** to reduce features to 2D.  
- Train a new SVM on 2D data.  
- Plot decision boundary, hyperplane, margins, and support vectors.

---

## Results
- **Accuracy**: ~96.5% on the test set.  
- **Classification Report**: Both classes achieved **precision & recall > 0.95**.  
- **Key Insight**: The dataset is well-suited for linear classifiers, with PCA visualization confirming classes are largely linearly separable.

---

## How to Run
1. Clone this repository:
   ```bash
   git clone <your-repo-link>
   cd <your-repo-name>
