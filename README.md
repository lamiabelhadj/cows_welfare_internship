# 🐄 Dairy Cattle Health State Prediction Using Machine Learning

## 🌿 Project Overview

This project focuses on understanding dairy cattle behavior in relation to health and welfare by leveraging sensor-based activity data and advanced machine learning techniques.  
The goal is to predict health conditions like **lameness**, **mastitis**, **oestrus**, and **calving** in real time to improve animal welfare, farm productivity, and operational efficiency.

The project builds upon the methodology of **Lardy et al. (2023)** and introduces enhanced data preparation, feature engineering, and classification pipelines, tested on real-world datasets from experimental and commercial farms.

---

## 📊 Key Features

- **Analysis of 4 publicly available datasets** from INRAE and commercial farms using Real-Time Location Systems (RTLS).  
- **Comprehensive data preparation pipeline**, including:
  - Cleaning and filtering based on data completeness.
  - Health-event label alignment and spreading.
  - Missing-label imputation with *K-Nearest Neighbors (K-NN)*.
  - One-hour shifting for time-series aggregation.
  - Data augmentation using *SMOTE-ENN* to address class imbalance.

- **Advanced Feature Engineering:**
  - Extraction of **32 time-series features** (statistical, dynamic, and frequency-based).
  - Feature selection using **SHAP values** and **Recursive Feature Elimination (RFE)**.

- **Multi-Model Evaluation:**
  - Tested models include *Random Forest*, *XGBoost*, *LightGBM*, *Bi-LSTM*, *MLP*, and *FT-Transformer*.
  - Hyperparameter tuning via *Grid Search* and *Cross-Validation*.
  - Pipeline comparison with and without data augmentation to assess robustness.

---

## 🔄 Pipeline Overview

This project implements two predictive pipelines:

### **Pipeline 1**
- Data Cleaning & Preparation  
- Feature Selection (SHAP values)  
- Classification using RF, XGBoost, LightGBM, Bi-LSTM, MLP, FT-Transformer  

### **Pipeline 2**
- Data Cleaning & Preparation  
- Data Augmentation (SMOTE-ENN)  
- Feature Selection (SHAP values)  
- Classification using RF, XGBoost, LightGBM, Bi-LSTM, MLP, FT-Transformer  

---

## 🧭 Branch Overview

| Branch | Purpose | Description |
|:-------|:---------|:-------------|
| **main** | 📘 Documentation & Structure | Central documentation and repository overview |
| **dev** | 🧪 Experimentation | Contains all iterative versions of notebooks, parameter tuning, and exploratory modeling work |
| **release-final** | 🚀 Clean Final Release | Contains the final, validated, and reproducible notebooks for each processing and modeling stage |

Each branch mirrors the same directory structure, ensuring traceability between experiments and the final release.

---

## 🛠️ Data Preparation and Modeling

Follow the same structured steps as defined in the project:

1. Data Cleaning & Health Event Alignment  
2. Label Imputation with K-NN  
3. One-Hour Shifting for Feature Aggregation  
4. Data Augmentation with SMOTE-ENN  
5. Feature Calculation (32 features)  
6. Feature Selection using SHAP   
7. Model Training with XGBoost, RF, LightGBM,  Bi-LSTM , MLP or FT-Transformer 
8. Model Evaluation (F1-scores, per-class performance)

---

## 🎯 Objectives

✅ Early detection of health and reproductive events in dairy cattle  
✅ Enhance predictive accuracy through robust data preparation and augmentation  
✅ Identify key behavioral indicators of health conditions  
✅ Develop scalable, non-invasive solutions for **Precision Livestock Farming (PLF)**  

---

## 📂 Dataset Overview

| Dataset | Source | # Cows | Duration | Notes |
|:--------|:--------|:-------|:----------|:-------|
| 1 | INRAE | 28 | 183 days | Rich in annotations (LPS) |
| 2 | INRAE | 28 | 60 days | Frequent acidosis cases |
| 3 | Commercial | 30 | 40–41 days | Oestrus-dominated |
| 4 | Commercial | ≈25 | 1 year | Large volume, imbalanced |

---

## 👥 Stakeholders

- 🧑‍🌾 **Dairy Farmers:** real-time health management  
- 🩺 **Veterinarians:** early disease detection support  
- 🔬 **Researchers:** enhancing PLF models  
- ⚙️ **Sensor / AgTech Companies:** system integration  

---

## 📚 References

- Lardy et al. (2023). *“Discriminating pathological, reproductive or stress conditions in cows using machine learning on sensor-based activity data.”*  
- INRAE Data Portal for dataset access.
