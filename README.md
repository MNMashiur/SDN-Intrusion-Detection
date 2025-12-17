# SDN-Intrusion-Detection
Machine Learning–Based Intrusion Detection System for Software-Defined Networks (SDN) using the InSDN dataset. This project evaluates multiple supervised ML models and ensemble techniques to detect SDN-specific cyberattacks, achieving high accuracy and robust generalization through careful preprocessing, feature selection, and model comparison.

# Machine Learning-Based Intrusion Detection System for Software-Defined Networks

## Overview
Software-Defined Networking (SDN) introduces centralized control and programmability, which improves network flexibility but also creates critical security vulnerabilities. A compromised SDN controller can impact the entire network, making effective intrusion detection essential.

This project presents a **machine learning–based Intrusion Detection System (IDS)** for SDN environments using the **InSDN dataset**. Multiple supervised learning models and ensemble techniques are evaluated to detect and classify malicious network traffic with high accuracy, robustness, and scalability.

The work is based on our academic research and experimental evaluation using real SDN traffic logs.

---

## Problem Statement
Traditional rule-based intrusion detection systems struggle to detect:
- New and evolving attack patterns  
- Complex and imbalanced SDN traffic  
- Non-linear relationships in high-dimensional flow data  

This project addresses these challenges by applying **machine learning and ensemble models** to flow-based SDN traffic for accurate intrusion detection.

---

## Key Features
- SDN-focused intrusion detection using real network flow data  
- Extensive data preprocessing and feature engineering  
- Handling of class imbalance using SMOTE  
- Feature selection using Random Forest importance  
- Comparison of multiple ML classifiers  
- Ensemble learning with Voting Classifier  
- Robust evaluation using test sets and cross-validation  

---

## Dataset
- **Dataset Name:** InSDN Dataset  
- **Source:** Kaggle  
- **Total Records:** ~343,939  
- **Features:** 84 flow-level features  
- **Attack Types:**  
  - Normal  
  - DoS  
  - DDoS  
  - Probe  
  - Brute Force Attack (BFA)  
  - Web Attack  
  - Botnet  
  - U2R  

The dataset contains realistic SDN traffic collected from Open vSwitch (OVS) and Metasploitable environments.

---

## Methodology

### 1. Data Preprocessing
- Removal of duplicate records  
- Handling missing values (mean for numerical, mode for categorical)  
- Encoding categorical features (Label Encoding & One-Hot Encoding)  
- Outlier capping using Z-score method  
- Feature standardization  

### 2. Feature Selection
- Correlation analysis to remove highly correlated features  
- Random Forest–based feature importance  
- Selection of top 48 most relevant statistical features  

### 3. Data Splitting
- 80% training / 20% testing split  
- Stratified sampling to preserve class distribution  

### 4. Model Training
The following models were implemented and evaluated:
- Logistic Regression  
- Decision Tree  
- Random Forest  
- Gradient Boosting  
- K-Nearest Neighbors (KNN)  
- Naive Bayes  
- XGBoost  
- Voting Classifier (Ensemble)  

---

## Results Summary
- **Best Cross-Validation Performance:**  
  - KNN (~96.05%)  
  - XGBoost (~94.37%)  
  - Random Forest (~92.21%)

- **Best Test ROC-AUC:**  
  - XGBoost (0.9470)

- Ensemble and tree-based models significantly outperform linear and probabilistic models.
- Cross-validation confirms that perfect training accuracy was caused by overfitting in some models, highlighting the importance of generalization.

---

## Technologies Used
- **Programming Language:** Python  
- **Libraries:**  
  - NumPy  
  - Pandas  
  - Scikit-learn  
  - XGBoost  
  - Matplotlib / Seaborn  

---

## Project Structure
