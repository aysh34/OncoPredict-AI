# Breast Cancer Detection Using Machine Learning  

[![Author: Ayesha Saleem](https://img.shields.io/badge/Author-Ayesha%20Saleem-orange?style=flat-square&logo=github)](https://github.com/aysh34)
[![Python](https://img.shields.io/badge/Python-3.8+-green.svg)](https://python.org)
[![Status](https://img.shields.io/badge/Status-Active-success.svg)]()


## Abstract  
Breast cancer remains one of the most common cancers worldwide, with early detection being essential for reducing mortality. This study applies machine learning techniques to classify breast tumors as malignant or benign using the **Breast Cancer Wisconsin (Diagnostic) Dataset**. Two models—**Logistic Regression** and **Random Forest** were developed and rigorously evaluated. Both models achieved high predictive performance, with Logistic Regression achieving an AUC of **0.9977** and Random Forest an AUC of **0.9929**. The results demonstrate the potential of machine learning to support clinical decision-making by reducing false negatives and improving diagnostic reliability.  

---

## Introduction  
Cancer diagnosis is traditionally based on manual interpretation of biopsies and imaging data, which can be time-consuming and prone to variability across practitioners. In contrast, machine learning algorithms can learn patterns from large-scale data, providing consistent, fast, and accurate predictions.  

This study develops a **machine learning pipeline** to detect breast cancer tumors. The models were trained to predict whether a tumor is **benign (0)** or **malignant (1)**, based on image-derived cellular features. The goal is to achieve **high sensitivity (recall)**, ensuring that malignant tumors are not misclassified as benign, as such errors can have life-threatening consequences.  

---

## Dataset Overview  
- **Name**: Breast Cancer Wisconsin (Diagnostic) Dataset  
- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic))  
- **Size**: 569 samples, 30 numerical features, and 1 target variable.  
- **Features**: Derived from digitized **fine needle aspirate (FNA) images** of breast masses. They describe cell nucleus characteristics such as:  
  - **Radius, Texture, Perimeter, Area** (structural features)  
  - **Smoothness, Compactness, Concavity** (shape descriptors)  
  - **Symmetry and Fractal Dimension** (geometric properties)  

For each feature, three statistical values are reported:  
- `_mean` (average),  
- `_se` (standard error),  
- `_worst` (worst-case value).  

**Target Variable**:  
- `diagnosis`: Malignant (1) or Benign (0).  

---

## Methodology  

### Workflow  
1. **Data Preprocessing**  
   - Dropped irrelevant columns (`id`, `Unnamed: 32`).  
   - Encoded `diagnosis` into binary labels (`M=1`, `B=0`).  
   - Standardized feature values using `StandardScaler`.  

2. **Exploratory Data Analysis (EDA)**  
   - Visualized class imbalance (357 benign vs 212 malignant).  
   - Analyzed feature distributions and correlations.  
   - Identified strong predictors such as `concave_points_worst`, `perimeter_worst`, and `radius_worst`.  

3. **Model Development**  
   - Implemented **Logistic Regression** and **Random Forest** classifiers.  
   - Performed **GridSearchCV** with cross-validation for hyperparameter tuning.  

4. **Evaluation**  
   - Assessed accuracy, precision, recall, F1-score.  
   - Generated confusion matrices.  
   - Computed ROC-AUC curves to measure discriminative ability.  

---

## Results  

### Logistic Regression  
- **Best Parameters**: `C=0.1`, `solver=liblinear`.  
- **Cross-Validation Accuracy**: **97.36%**.  
- **Test Accuracy**: **98.25%**.  
- **AUC**: **0.9977**.  

**Classification Report:**  
- Precision: 1.00 (malignant), 0.97 (benign).  
- Recall: 0.95 (malignant), 1.00 (benign).  
- Balanced F1-score across classes.  

---

### Random Forest  
- **Best Parameters**: `n_estimators=100`, `max_features='sqrt'`, `max_depth=None`.  
- **Cross-Validation Accuracy**: **96.26%**.  
- **Test Accuracy**: **97.37%**.  
- **AUC**: **0.9929**.  

**Classification Report:**  
- Precision: 1.00 (malignant), 0.96 (benign).  
- Recall: 0.93 (malignant), 1.00 (benign).  

---

### Visualizations  
- **Confusion Matrices**: Both models had minimal misclassifications, with Logistic Regression slightly outperforming Random Forest in recall for malignant cases.  
- **ROC Curves**: Both models demonstrated near-perfect separability, with Logistic Regression showing marginally superior AUC.  

---

## Discussion  
Both Logistic Regression and Random Forest classifiers performed exceptionally well. Importantly, **recall values were prioritized**, since failing to detect malignant tumors is clinically unacceptable. Logistic Regression, despite being simpler and more interpretable, achieved slightly better discriminative performance compared to Random Forest.  

The feature importance analysis confirmed prior medical knowledge: features related to **tumor size and shape irregularities** (e.g., perimeter, concavity, radius) strongly correlated with malignancy.  

---

## Conclusion  
This study demonstrates the feasibility of using machine learning for breast cancer detection. Both models achieved accuracy above **97%** with near-perfect AUC scores. Logistic Regression proved to be both **accurate and interpretable**, making it a practical choice for medical diagnostic tools.  

---

## References  
1. Street, W. N., Wolberg, W. H., & Mangasarian, O. L. (1993). *Nuclear feature extraction for breast tumor diagnosis*. IS&T/SPIE International Symposium on Electronic Imaging.  
2. UCI Machine Learning Repository: Breast Cancer Wisconsin (Diagnostic) Dataset. [Link](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic))  
