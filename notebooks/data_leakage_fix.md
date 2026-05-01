# Data Leakage Investigation and Fix

## Overview

During the initial development and deployment phase of the Ride Cancellation Prediction project, multiple machine learning models were trained and evaluated, including Logistic Regression, Decision Tree, and Random Forest. Although these models achieved unusually high accuracy scores, their precision and recall metrics were significantly low and unstable.

This inconsistency indicated a potential issue with data leakage and poor generalization capability.

---

## Initial Observations

In the first iteration:

- Multiple models (Logistic Regression, Decision Tree, Random Forest) showed **very high accuracy**
- However, **precision and recall scores were significantly low**
- Models failed to generalize to unseen data
- Logistic Regression was selected for MVP deployment due to being the most stable among weak-performing models

Despite this, even the deployed MVP on Hugging Face Spaces produced unreliable and inconsistent predictions. To ensure a working demo, a simplified fallback logic was temporarily implemented that was not truly representative of the trained model behavior.

---

## Problem Identification

After revisiting the dataset and training pipeline, a deeper analysis revealed:

- Presence of **data leakage features**
- Features that indirectly contained target-related information
- Noisy variables negatively affecting model learning
- Overly optimistic performance due to leakage rather than real predictive power

These issues caused the model to memorize patterns instead of learning generalizable relationships.

---

## Root Cause

The main issues were:

- Inclusion of features that were directly or indirectly correlated with the target variable in a way that would not exist in real-world prediction time
- Lack of proper feature validation before training
- Insufficient separation between informative vs. leaking variables
- Noise in original feature set masking true signal distribution

---

## Solution Approach

A full feature engineering and dataset reconstruction process was applied:

### 1. Feature Audit
All existing features were carefully analyzed to identify:
- Leakage-prone variables
- Redundant or highly correlated features
- Noise-heavy attributes

### 2. Removal of Leakage Features
Features identified as leaking target information were removed from the dataset to prevent artificial performance inflation.

### 3. Safe Feature Engineering
Instead of simply dropping information, new **safe and meaningful features** were engineered to preserve predictive signal without introducing leakage.

### 4. Noise Reduction
Noisy and low-signal features were eliminated or transformed to improve model stability.

---

## Final Dataset

After cleaning and feature reconstruction:

- A **leakage-free dataset** was created
- Predictive signal was preserved through engineered safe features
- Data distribution was improved to better reflect real-world conditions
- The dataset was prepared for reliable future model training

---

## Outcome

- Identified and removed sources of artificial performance inflation caused by data leakage  
- Improved data quality and feature reliability  
- Established a clean and consistent dataset for subsequent modeling stages  
- Strengthened the overall machine learning pipeline before model re-training  

---

## Key Learning

This phase highlighted that:

> High accuracy alone is not a reliable indicator of model quality. Proper feature validation, leakage detection, and dataset integrity are essential before proceeding to model development in production-grade machine learning systems.
