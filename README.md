
# Dairy Cattle Health State Prediction Using Machine Learning

## 🐄 Project Overview

This project focuses on understanding dairy cattle behavior in relation to health and welfare by leveraging sensor-based activity data and advanced machine learning techniques. The goal is to predict health conditions like lameness, mastitis, oestrus, and calving in real time to improve animal welfare, farm productivity, and operational efficiency.

The project builds upon the methodology of Lardy et al. (2023) and introduces enhanced data preparation, feature engineering, and classification pipelines, tested on real-world datasets from experimental and commercial farms.

## 📊 Key Features

- Analysis of 4 publicly available datasets from INRAE and commercial farms using Real-Time Location Systems (RTLS).
- Comprehensive data preparation pipeline including:
  - Cleaning and filtering based on data completeness.
  - Health event label alignment and spreading.
  - Missing label imputation with K-Nearest Neighbors (K-NN).
  - One-hour shifting for time-series aggregation.
  - Data augmentation using SMOTE-ENN to address class imbalance.

- Advanced Feature Engineering:
  - Extraction of 32 time-series features (statistical, dynamic, and frequency-based).
  - Feature selection using SHAP values and Recursive Feature Elimination (RFE).

- Multi-Model Evaluation:
  - Tested models include Random Forest, XGBoost, LightGBM, and Bi-LSTM.
  - Hyperparameter tuning via Grid Search and Cross-Validation.
  - Pipeline comparison with and without data augmentation to assess robustness.
  ## 🔄 Pipeline Overview

This project implements two predictive pipelines in the first place:

**Pipeline 1:**
- Data Cleaning & Preparation
- Feature Selection (SHAP values)
- Classification using RF, XGBoost, LightGBM, Bi-LSTM

**Pipeline 2:**
- Data Cleaning & Preparation
- Data Augmentation (SMOTE-ENN)
- Feature Selection (SHAP values)
- Classification using RF, XGBoost, LightGBM, Bi-LSTM

## 🚀 Project Structure

```

├── data/
│   ├── dataset1.csv
│   ├── dataset2.csv
│   ├── dataset3.csv
│   ├── dataset4.csv
│   └──preprocessed datasets
├── EDA/
│   ├── EDA_merged.ipynb
├── README.md
└── requirements.txt
```

## 🛠️ How to Run

1. **Requirements**  
   Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

2. **Exploratory Data Analysis (EDA)**  
   The EDA notebook is function-based. You can easily run it on all four datasets:

   ```python
   datasets = [
       'data/dataset1.csv',
       'data/dataset2.csv',
       'data/dataset3.csv',
       'data/dataset4.csv'
   ]

   for file in datasets:
       print(f"Processing {file}")
       df = load_dataset(file)
       check_missing_values(df)
       date_coverage_check(df)
       plot_numeric_distributions(df)
       correlation_analysis(df)
   ```

3. **Data Preparation and Modeling**  
   Follow the same structured steps as defined in the project:
   
   - Data Cleaning & Health Event Alignment
   - Label Imputation with K-NN
   - One-Hour Shifting for feature aggregation
   - Data Augmentation with SMOTE-ENN
   - Feature Calculation (32 features)
   - Feature Selection using SHAP or RFE
   - Model Training with XGBoost, RF, LightGBM, or Bi-LSTM
   - Model Evaluation (F1-scores, per-class performance)

## 🎯 Objectives

✅ Early detection of health and reproductive events in dairy cattle  
✅ Enhance predictive accuracy through robust data preparation and augmentation  
✅ Identify key behavioral indicators of health conditions  
✅ Develop scalable, non-invasive solutions for Precision Livestock Farming (PLF)  

## 📂 Dataset Overview

| Dataset | Source     | # Cows | Duration  | Notes                   |
|---------|------------|--------|-----------|-------------------------|
| 1       | INRAE      | 28     | 183 days  | Rich in annotations, LPS |
| 2       | INRAE      | 28     | 60 days   | Frequent acidosis cases |
| 3       | Commercial | 30     | 40-41 days| Oestrus-dominated       |
| 4       | Commercial | ~25    | 1 year    | Large volume, imbalanced |

## 👥 Stakeholders

- Dairy Farmers for real-time health management  
- Veterinarians for early disease detection support  
- Researchers enhancing PLF models  
- Sensor/AgTech Companies for system integration  


## 📚 References

- Lardy et al. (2023). "Discriminating pathological, reproductive or stress conditions in cows using machine learning on sensor-based activity data."  
- INRAE Data Portal for dataset access.
