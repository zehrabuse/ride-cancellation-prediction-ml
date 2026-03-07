# Ride Cancellation Business Insights Documentation

## Purpose

This notebook (` [RDP_Business_Insights.ipynb](notebooks/RDP_Business_Insights.ipynb)`) provides a comprehensive analysis of ride cancellations from a processed ride-hailing dataset. The goal is to extract **business-relevant insights**, identify key factors influencing cancellations, and provide actionable recommendations for improving **platform reliability, customer satisfaction, and driver efficiency**.

## Notebook

You can view and run the notebook here: ` [RDP_Business_Insights.ipynb](notebooks/RDP_Business_Insights.ipynb)`

## Steps Taken

1. **Ride Cancellation Patterns**

   * Counted completed vs cancelled rides.
   * Determined share of cancellations initiated by drivers vs customers.
   * Interpreted potential causes: low expected earnings, vehicle issues, trip distance.

2. **Temporal Analysis**

   * Analyzed cancellations by hour, day of week, and month.
   * Identified peak hours (18:00–20:00), weekdays (especially Monday), and months (May, July) with higher cancellations.
   * Considered customer and driver behaviors influencing these trends.

3. **Vehicle Type Analysis**

   * Examined cancellation rates by vehicle type.
   * Found Go-Sedan vehicles have higher cancellations.
   * Possible causes: maintenance issues, fuel consumption, low profitability.

4. **Payment Method Analysis**

   * Analyzed cancellations by payment method.
   * Identified UPI as the most cancellation-prone method.
   * Possible causes: technical issues or new implementation challenges.

5. **Observations & Business Implications**

   * Driver-related factors, vehicle type, peak hours, and payment methods are significant drivers of cancellations.
   * Customer behavior, seasonal trends, and operational constraints also play important roles.

6. **Recommendations**

   * Introduce driver incentives for high-risk trips.
   * Perform regular vehicle maintenance.
   * Apply customer-focused promotions during peak times and for larger vehicles.
   * Resolve technical issues with UPI or consider alternative payment methods.

## Output

Summarized tables and plots highlighting cancellation trends, temporal patterns, vehicle types, and payment method issues, along with actionable business recommendations.

*This documentation accompanies the `RDP_Business_Insights.ipynb` notebook and is intended for portfo
