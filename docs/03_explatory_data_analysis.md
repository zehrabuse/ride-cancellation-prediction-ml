# Ride Cancellation EDA Documentation

## Purpose
This notebook (**notebooks/RDP_EDA.ipynb**) provides a comprehensive exploratory analysis of the ride cancellation dataset. The goal is to identify patterns, trends, and key features influencing cancellations, which will guide subsequent feature engineering and predictive modeling.

## Notebook
You can view and run the notebook here: **notebooks/RDP_EDA.ipynb**

## Steps Taken

### 1. Temporal Analysis
- Converted `Year`, `Month`, `Day`, `Hour`, `Minute` columns into **datetime format** (`booking_time`).
- Created additional time-based features:
  - `hour_minute` – hour and minute combination
  - `time_15min` – 15-minute intervals
  - `Day` – day of the month
  - `day_of_week` – day of the week
  - `week_part` – weekday vs weekend
- Analyzed cancellations over time using **line plots** and **bar plots**.

### 2. Day-wise Cancellation Analysis
- Counted cancellations by **day of the month** to find peak dates.
- Counted cancellations by **day of the week** to identify weekly patterns.
- Compared **weekdays vs weekends** to see which period has higher cancellations.
- Visualized results with bar plots for clarity.

### 3. Categorical Feature Analysis
- Analyzed **one-hot encoded features**:
  - Vehicle Type – calculated cancellation rate per vehicle type.
  - Payment Method – calculated cancellation rate per payment method.
- Transformed one-hot encoded columns to **long format** for meaningful aggregation.
- Visualized high-risk categories using bar plots.

### 4. Observations
- Identified peak cancellation times and 15-minute intervals.
- Determined which days of the month and week have higher cancellation rates.
- Found vehicle types and payment methods most associated with cancellations.

## Output
- Plots and tables summarizing cancellation trends over time and across categorical features.
