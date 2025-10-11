# 🧪 Cows Welfare Internship — Development Branch (All Versions)

## 🌿 Overview
This branch (`dev`) serves as the **development workspace** of the *Cows Welfare Internship* project.  
It mirrors the structure of the `release-final` branch but retains **all intermediate versions**, **experimental notebooks**, and **variant code implementations** used during the research and model development process.

While `release-final` consolidates the **clean, reproducible pipeline**, this branch documents the **journey of experimentation** — from preprocessing trials and feature-engineering ideas to model tuning and architectural tests.

---

## 🧭 Project Structure

### 📁 **1. Data imbalance/**
> Includes multiple iterations of imbalance handling methods and comparison experiments.

Contains:
- Different versions of SMOTE ENN function based notebooks.
- Final integration notebook used later in `release-final`.


---

### 📁 **2. EDA/**
> All exploratory analysis versions before final optimization.

Contains:
- Early visualizations of cow activity distributions.  
- Multiple drafts of feature correlation analysis and missing-value heatmaps.  
- Function-based EDA versions that evolved into the final modular notebook.  

*(Purpose: experiment with visualization formats, normalization schemes, and automatic summary generation.)*

---

### 📁 **3. Preprocessing/**
> Central area of experimentation, with numerous subfolders tracking the evolution of the preprocessing pipeline.

#### 📂 Cleaning/
- Early versions testing rule-based filtering and statistical thresholds.  
-Different function-based notebooks versions.
#### 📂 Feature engineering/
- Different transformation trials in a modular way.

#### 📂 Feature selection/
- SHAP feature selection versions.  

#### 📂 Transformation/
- KNN reassignmenet and episodes alignment. 


---

### 📁 **4. Modeling/**
> Contains all experiments and model prototypes, each with multiple versions and parameter trials.

#### 🔹 **Random Forest/**
- Validation runs on multiple dataset splits.  


#### 🔹 **XG_Boost/**
- Verification of performance across all datasets.

#### 🔹 **LightGBM/**
- Verification of performance across all datasets.

#### 🔹 **MLP_non_augmented/**
- Multiple network depths (2 to 3 layers), dropout variations, and activation functions.  
- Optimizer trials (Adam, AdamW, RMSprop) with different schedulers (StepLR, OneCycleLR).  
- Baseline vs tuned hyperparameter versions.

#### 🔹 **MLP_augmented/**
- Retraining with augmented data and adaptive learning-rate schedulers.  
- Early experiments with class-weighted losses and Focal Loss.  
- Training visualizations (loss/F1 curves, confusion matrices).

#### 🔹 **FT_transformer_augmented/**
- Progressive iterations of the FT-Transformer model architecture:  
  * token embedding tweaks, positional encodings, layer depth variations, and dropout tuning.  
- Experiments on batch size, warmup steps, and learning rates.  
- Trials integrating mixup regularization and EMA updates.

*(Purpose: record of all experimental architectures, hyperparameter tuning, and evaluation logs.)*

---

### 📁 **5. Results/**
> Logs, intermediate transformations, and comparison notebooks for model evaluation.


*(Purpose: archive of iterative evaluation phases leading to the final selected models.)*

---

### 📁 **6. Extra/**
> Helper utilities, data manipulation, and splitting data scripts.


---

### 📄 **Other Files**
- **.gitignore** – Similar to `release-final`, but may include extended ignores for temporary experiments.  
- **README.md** – This documentation file describing development organization.  

---

## ⚙️ Branch Details
- **Branch name:** `dev`  
- **Last updates:** iterative commits throughout model development  
- **Commit density:** very high — reflects continuous experimentation and tuning cycles  
- **Purpose:** document all technical decisions, failed attempts, and alternative configurations leading up to the final release.

---

## 🧩 Relationship to `release-final`
| Aspect | `dev` Branch | `release-final` Branch |
|:--|:--|:--|
| Objective | Exploration & experimentation | Stability & reproducibility |
| Code Versions | Multiple, incremental | Single, clean, validated |
| Structure | Same modular hierarchy | Same structure (final selected notebooks only) |
| Focus | Tuning, testing, debugging | Documentation, presentation, reproducibility |
| Status | Active during development | Locked post-validation |

---

## 📘 Notes
- This branch is **essential for traceability**, showing the evolution of every notebook and function.  
- It enables **auditability** of how final preprocessing and model choices were derived.  
- Ideal for internal review, reproducibility tests, or research audits.

---

## 👩‍🔬 Author
**Lamia Belhadj**  
Cows Welfare Internship — *Development Branch (All Versions)*  
Maintained on DagsHub | Git-integrated for full experiment history.
