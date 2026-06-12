# GeneXplain: Explainable AI Framework for Genetic Disease Prediction using Genomic Biomarkers

**Author:** Arif 

---

# Project Timeline & Milestones

###  Week 1: Environment Setup & Project Architecture 
* **Environment Configuration:** Initialized the Google Colab development runtime ecosystem.
* **Storage Mapping:** Linked Google Drive virtual file systems with absolute paths for raw datasets and tracking directories.
* **Directory Structuralization:** Programmatically created production-grade folder architectures:
  ```text
  GeneXplain/
  ├── notebooks/       # Google Colab development scripts
  ├── datasets/        # Processed train/validation/test CSV splits
  └── visualizations/  # Statistical analysis, EDA plots, and heatmaps

###  Week 2: Dataset Collection, EDA, and Preprocessing 
* **Pipeline Integration:** Automated data collection and handled clinical target value cleansing (Mapping to 0: Benign, 1: Malignant).
* **Feature Normalization:** Applied robust Z-Score Standardization ($\mu = 0, \sigma^2 = 1$) across features to preserve gradient weightings.
* **Two-Stage Feature Selection ($p \gg n$):** Utilized a `VarianceThreshold` filter and an ANOVA F-Test (`SelectKBest`) to successfully isolate 9 core prognostic features.
* **Leak-Proof Stratification:** Segmented samples into isolated, stratified matrices (**70% Train**, **15% Val**, **15% Test**) to prevent data leakage.

### 🔹 Week 3: Baseline Model Development & Evaluation (Completed)
* **Model Implementation:** Programmatically trained three distinct core baseline machine learning classifiers: **Logistic Regression**, **Random Forest**, and **XGBoost**.
* **Metrics Extraction:** Successfully extracted performance metrics evaluating model Accuracy, Precision, Recall, F1-Score, and ROC-AUC metrics.
* **Error Diagnosis:** Generated and exported automated validation confusion matrices into the `visualizations/confusion_matrices/` repository folder to track diagnostic classification errors.

> ** Champion Selection Result:** **Random Forest** has been selected as the project's **Champion Model** moving forward. Out of the box, it achieved the highest overall structural balance with an **Accuracy of 0.9714** and a dominant **F1-Score of 0.9600**, alongside a flawless clinical **Recall score of 1.0000** (zero False Negatives) and high threshold stability (**ROC-AUC: 0.9919**).

###  Week 4: Hyperparameter Tuning & Model Optimization 
* **Optimization Framework:** Executed structured hyperparameter search strategies over tree depth, learning rates, estimator counts, and regularization settings.
* **Overfitting Mitigation:** Tuned structural boundaries and validation splits to significantly minimize performance gaps between training and validation cohorts.
* **Champion Model Selection:** Conducted final comparative evaluation to lock in the absolute highest-performing configuration for downstream Explainable AI (XAI) feature tracking.
  
