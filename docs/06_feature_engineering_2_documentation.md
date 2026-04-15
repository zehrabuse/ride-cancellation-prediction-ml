# Feature Engineering 2 Documentation

## Purpose
This notebook (**RDP_Feature_Engineering_2.ipynb**) refines the feature engineering process by addressing data leakage issues discovered in the previous modeling phase.

Although the initial model built on Feature Engineering_1 achieved high accuracy, it failed to generalize properly, indicating leakage in the feature set. This notebook focuses on correcting these issues and producing a reliable, model-ready dataset.

---

## Notebook
You can view and run the notebook here: [RDP_Feature_Engineering_2.ipynb](../notebooks/RDP_Feature_Engineering_2.ipynb)


## Steps Taken

### 1. Data Leakage Detection & Fixing
- Identified features causing data leakage from the previous feature engineering stage  
- Removed leakage-prone variables that contained post-event or outcome-related information  
- Ensured all remaining features are available at prediction time  

---

### 2. Target Engineering
- Created a refined multi-class target variable (**new_target**)  
- Converted the original binary structure into:
  - No cancellation  
  - Cancelled by Customer  
  - Cancelled by Driver  
- Removed the original **target** column after transformation to avoid redundancy  

---

### 3. Feature Cleaning & Removal
- Removed redundant cancellation-related columns after target creation  
- Dropped **Avg VTAT** and **Avg CTAT** due to data leakage risk  
- Removed **Minute**, **Year**, and **Day** features due to low predictive value or noise  

---

### 4. Rating Feature Engineering
- Transformed **Customer Rating** and **Driver Ratings** into categorical risk levels (Low / Medium / High)  
- Created **high_risk_pair** feature to capture interactions between low-rated drivers and customers  
- Dropped original rating columns after transformation  

---

### 5. Time-Based Feature Engineering
- Created **rush_hour** (17–20) and **late_night** (00–05) features  
- Engineered **weekend_rush** interaction feature  
- Removed unnecessary granular time features to reduce noise  

---

### 6. Pricing & Distance Features
- Created **price_per_km** to normalize booking value by ride distance  
- Replaced infinite values (inf, -inf) with NaN for numerical stability  
- Engineered **distance_high_price** to capture high-value long-distance rides  

---

### 7. Feature Validation
- Checked dataset for missing (NaN) and infinite (inf) values  
- Ensured data consistency and stability before modeling  

---

## Output
The final processed dataset is saved as:

**final_dataset.csv**

This dataset:
- Is free from data leakage  
- Contains engineered and meaningful features  
- Is cleaned from redundant and noisy variables  
- Is fully model-ready for machine learning tasks  
