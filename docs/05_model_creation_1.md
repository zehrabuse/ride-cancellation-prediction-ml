# Model Creation Documentation

## Purpose
This notebook (`RDP_Model_Creation_1.ipynb`) focuses on building and evaluating predictive models for ride cancellations. The goal is to create an MVP-ready model and explore alternative models for potential improvement.

## Notebook
You can view and run the notebook here: [RDP_Model_Creation_1.ipynb](../notebooks/RDP_Model_Creation_1.ipynb)

## Dataset Versions
- **v2:** Dataset after removing `booking_status` column. This version was used to ensure no leakage from the original target.
- **v3:** Final processed dataset (`ride_cancellation_processed_v3.csv`) used for model training, after removing features derived from the target (`Cancelled Rides by Driver`, `Cancelled Rides by Customer`) to prevent data leakage, while keeping all other predictive features intact.

## Steps Taken

### Data Preparation
- Loaded the cleaned dataset `ride_cancellation_processed_v3.csv`.
- Dropped columns that could cause data leakage (e.g., `Cancelled Rides by Driver`, `Cancelled Rides by Customer`) while preserving features necessary for future analysis.
- Applied train-test split to create separate datasets for training and evaluation.
- Standardized features for Logistic Regression; scaling not applied for tree-based models (Decision Tree, Random Forest) as it is unnecessary.

### Baseline Model: Logistic Regression
- Trained with **LBFGS** and **SAGA** solvers.
- Used common parameters: `max_iter=5000`, `solver`, `C=1.0`, `penalty='l2'`, `random_state=42`.
- Evaluated using accuracy, precision, recall, F1 score, and ROC-AUC.
- Observed that Logistic Regression produced stable and interpretable performance, suitable for MVP deployment.

### Tree-Based Models
- **Decision Tree** and **Random Forest** trained without feature scaling.
- Achieved near-perfect precision and recall for both classes.
- High performance indicates potential **overfitting** or residual **data leakage**.
- Random Forest included parameters like `n_estimators=100`, `max_depth=10`, `min_samples_split=10`, `min_samples_leaf=5`, and `random_state=42` to improve generalization.

### Model Evaluation
- Logistic Regression: stable, interpretable performance.
- Tree-based models: very high accuracy, precision, and recall, but with overfitting risk.
- ROC & AUC curves calculated for all models to assess classification performance.

### MVP Decision
- Chose **Logistic Regression** for MVP due to reliable performance on unseen data.
- Tree-based models will be revisited after further preprocessing and validation to potentially enhance predictions.

## Output
- Model evaluation metrics (accuracy, precision, recall, F1, ROC-AUC) recorded in the notebook.
- Logistic Regression selected as **MVP-ready model**.
