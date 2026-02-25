# Data Cleaning Documentation

## Purpose
This notebook(`RDP_Data_Cleaning.ipynb`) focuses on cleaning the raw ride dataset to handle missing values and prepare it for feature engineering.

## Notebook
You can view and run the notebook here: [RDP_Data_Cleaning.ipynb](../notebooks/RDP_Data_Cleaning.ipynb)

## Steps Taken

### Target Column
- Booking_status had five categories: Completed, Incomplete, No Driver Found, Cancelled by Driver, Cancelled by Customer.
- Incomplete and No Driver Found records were removed to improve data quality.
- Target defined as: Cancelled by Driver or Cancelled by Customer → 1, Completed → 0.
- Original booking_status column dropped to prevent data leakage.

### Missing Values
- Binary event flag columns (Cancelled Rides, Incomplete Rides): NaN → 0
- Numerical continuous columns (Avg VTAT, Driver Ratings, etc.): Median imputation
- Categorical columns (if any): Mode imputation

### Columns Removed
- Booking ID & Customer ID: Identifiers, removed to prevent overfitting
- Pickup & Drop Location: High cardinality, removed to reduce model complexity

## Output
- Cleaned dataset saved as `ride_cancellation_cleaned.csv`
