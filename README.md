# 🧠 OncoPredict AI – Breast Cancer Detection with Machine Learning
![Python](https://img.shields.io/badge/python-3.8%2B-blue?style=flat-square)
![Platform](https://img.shields.io/badge/platform-Jupyter%20%7C%20Python%20-bue?style=flat-square)
![Status](https://img.shields.io/badge/status-active-blue?style=flat-square)

**OncoPredict AI** is a machine learning-based diagnostic system designed for **early and accurate detection of breast cancer**. Built using the Breast Cancer Wisconsin (Diagnostic) Dataset, it classifies tumors as **benign** or **malignant** based on digitized image features of cell nuclei, supporting better and faster clinical decision-making.

This project not only includes a detailed analytical notebook but also features an interactive **Streamlit web application** for real-time predictions.

---

## 🚀 Key Features

-   📊 Full machine learning pipeline: preprocessing → EDA → modeling → evaluation.
-   🧪 Minimizes false negatives, crucial for safe medical predictions.
-   🤖 Dual-model setup: **Logistic Regression** & **Random Forest** for robust predictions.
-   📈 Comprehensive evaluation includes ROC-AUC, confusion matrix, precision, recall, and F1-score.
-   🌐 **Interactive Streamlit App:** Easily demonstrate predictions and explore model performance.

---

## 📌 Dataset

-   **Name:** Breast Cancer Wisconsin (Diagnostic) Dataset
-   **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic))
-   **Type:** Supervised binary classification
-   **Samples:** 569 instances
-   **Features:** 30 numerical features computed from digitized images of fine needle aspirates (FNA) of breast masses (e.g., `radius_mean`, `texture_mean`, `perimeter_worst`, `concave points_mean`).
-   **Target:** Diagnosis (`M` = Malignant, `B` = Benign)

---

## 📊 Workflow

### 🔍 1. Exploratory Data Analysis (EDA)
-   Distribution analysis of the target variable (class balance check).
-   KDE plots and histograms to visualize feature distributions by diagnosis.
-   Correlation heatmap to identify relationships between features.
-   Analysis of feature correlation with the target variable (`diagnosis`).

### 🛠️ 2. Data Preprocessing & Feature Engineering
-   Handling of missing values (dropping `Unnamed: 32` column).
-   Removal of irrelevant identifiers (dropping `id` column).
-   Label encoding for the target variable (`diagnosis`: M=1, B=0).
-   Splitting the dataset into training and testing sets (80% train, 20% test) with stratification to maintain class proportions.
-   Feature scaling using `StandardScaler` to standardize numerical features, applied separately to training and testing sets to prevent data leakage.

### 🤖 3. Modeling & Optimization
-   **Model Selection:**
    -   **Logistic Regression:** Chosen as a strong baseline, offering interpretability and efficiency.
    -   **Random Forest Classifier:** A robust ensemble method known for high performance and handling complex relationships.
-   **Hyperparameter Tuning:** `GridSearchCV` is employed to systematically search for the optimal hyperparameters for both models.
-   **Cross-Validation:** 5-fold cross-validation is integrated into `GridSearchCV` to ensure model robustness and reliable performance estimates.

### 📈 4. Evaluation Metrics
-   **Accuracy Score:** Overall proportion of correct predictions.
-   **Classification Report:** Provides detailed Precision, Recall, and F1-score for each class.
    -   **Precision:** Crucial for minimizing false positives (e.g., preventing unnecessary invasive procedures).
    -   **Recall:** Paramount in medical diagnosis for minimizing false negatives (e.g., not missing actual cancer cases).
-   **Confusion Matrix:** Visual representation of True Positives, True Negatives, False Positives, and False Negatives.
-   **Receiver Operating Characteristic (ROC) Curve & Area Under the Curve (AUC):** Measures the model's ability to discriminate between positive and negative classes across various thresholds.

---

## 🧪 Installation & Usage

To get started with this project, follow these steps:

### Requirements

Ensure you have Python 3.8+ installed. All required libraries can be installed using pip:

```bash
pip install -r requirements.txt
