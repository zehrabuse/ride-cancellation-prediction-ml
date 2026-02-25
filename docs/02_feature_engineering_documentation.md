# Feature Engineering Documentation

## Purpose
This notebook converts the cleaned dataset into a model-ready dataset with feature extraction and encoding.

## Steps Taken

### Temporal Features
- Date & Time converted to datetime format
- Extracted features: Year, Month, Day, Day_of_week, Hour, Minute, Is_weekend
- Original Date & Time columns dropped after extraction

### Encoding Categorical Variables
- Vehicle Type → One-Hot Encoding (converted to 0/1)
- Payment Method → One-Hot Encoding (converted to 0/1)

### Columns Removed
- Reason for Customer Cancelling, Driver Cancellation Reason, Incomplete Rides Reason: Removed to prevent data leakage

## Output
- Final processed dataset saved as `ride_cancellation_processed.csv`
