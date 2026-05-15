# Model Creation Documentation (Part 2)

## Purpose
This notebook (**RDP_Model_Creation_2.ipynb**) focuses on rebuilding and re-evaluating machine learning models for ride cancellation prediction after identifying and resolving a data leakage issue in the previous modeling phase. The objective is to ensure a more reliable, realistic, and production-ready modeling pipeline through improved feature engineering and corrected dataset design.

The main goal of this stage is to validate model performance after leakage removal and select the most suitable final model based on robust evaluation metrics.

---

## Notebook
You can view and run the notebook here: [RDP_Model_Creation_2.ipynb](../notebooks/RDP_Model_Creation_2.ipynb)


---

## Dataset Versions

- **v3 (Corrected Dataset):** Final processed dataset used in this notebook after fixing data leakage issues identified in the previous version.
  
  Key corrections include:
  - Removal of leakage-related features that directly or indirectly encoded the target variable
  - Refinement of feature engineering pipeline (Feature Engineering 2)
  - Ensuring strict separation between predictive features and target variable (`new_target`)

This version is considered the most reliable dataset for final model training and evaluation.

---

## Steps Taken

### Data Preparation
- Loaded the corrected dataset (`final_dataset.csv`)
- Selected a refined feature set including:
  - Trip characteristics (distance, time, booking value)
  - Temporal features (hour, day, month, weekend indicators)
  - Engineered risk features (high-risk pair, rush hour, late night)
  - Customer and driver rating distributions
  - Encoded categorical variables (vehicle type, payment method)
- Defined target variable as `new_target`
- Applied stratified train-test split (80/20) to preserve class distribution
- Applied feature scaling using StandardScaler for Logistic Regression, while tree-based models were trained without scaling

---

### Baseline Model: Logistic Regression
- Trained as a baseline classifier using scaled features
- Configured with:
  - LBFGS solver
  - max_iter=5000
  - class_weight="balanced"
  - random_state=42
- Evaluated using:
  - Accuracy
  - Precision
  - Recall
  - F1-score
  - ROC-AUC

Logistic Regression provided stable and interpretable results, serving as a benchmark for comparison.

---

### Tree-Based Models

#### Decision Tree
- Trained without feature scaling
- Configured with class balancing and fixed random state
- Captured non-linear relationships in the dataset
- Provided interpretable decision rules but showed sensitivity to data variation

#### Random Forest
- Trained using ensemble learning approach with multiple decision trees
- Configured with:
  - n_estimators=300
  - class_weight="balanced"
  - random_state=42
- Delivered the strongest overall performance across evaluation metrics
- Demonstrated robustness in handling complex feature interactions

---

## Model Evaluation
All models were evaluated using:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- ROC-AUC (multiclass OvR approach)

Key observations:
- Logistic Regression provided stable baseline performance
- Decision Tree showed moderate improvement but higher variance
- Random Forest achieved the best overall performance, especially in recall and ROC-AUC scores

---

## Final Model Decision
Random Forest was selected as the final model for deployment.

### Reasons:
- Highest overall predictive performance
- Strong recall across all classes (critical for cancellation prediction)
- Robustness to feature complexity and non-linear relationships
- Stable cross-validation performance compared to other models

---

## Output
- Final trained models stored within the notebook
- Evaluation metrics recorded for all models
- Random Forest selected as the final production-ready model for deployment
