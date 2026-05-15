# Ride Cancellation Prediction – Machine Learning Project

## Project Overview
This project aims to predict the probability of ride cancellations using machine learning techniques. The project follows an end-to-end machine learning pipeline, starting from business problem definition to model deployment and result visualization.

---

## Project Status
Completed – The project is fully implemented as an end-to-end machine learning system, including data processing, model development, evaluation, and deployment.

---

## Business Problem
Ride cancellations negatively affect customer satisfaction and operational efficiency. By predicting cancellation probability in advance, companies can take proactive actions to reduce cancellations and improve service quality.

---

## Business Objectives
Detailed documentation of the business objectives, decision support perspective, and expected business impact of this project is available below:

- 📄 [Business Objectives Documentation](docs/business_objectives.md)  
- 📊 [Business Value & Success Metrics](docs/business_value_and_metrics.md)

---

## Data Preparation & Feature Engineering Documentation

### 📄 Data Cleaning Documentation
This document focuses on handling missing values in the dataset. It explains how missing values were identified and how they were handled to improve data quality and prepare the data for modeling.

[01_cleaning_documentation.md](docs/01_cleaning_documentation.md)

---

### 📄 Feature Engineering Documentation
This document covers the feature engineering process applied to the dataset. It includes data type corrections, encoding of categorical variables, and basic feature transformations performed to make the dataset suitable for machine learning algorithms.

[02_feature_engineering_documentation.md](docs/02_feature_engineering_documentation.md)

Additionally, this stage was revisited after identifying a data leakage issue in the dataset. A second feature engineering iteration was performed to eliminate leakage risks and ensure data integrity, resulting in a more robust and reliable feature set.

[06_feature_engineering_2.md](docs/06_feature_engineering_2.md)
---

### 📄 Exploratory Data Analysis
This repository includes a comprehensive exploratory analysis of the ride cancellation dataset. The EDA notebook identifies patterns, trends, and key features influencing cancellations, which helps guide feature engineering and predictive modeling.

You can view and run the notebook here:  
[03_exploratory_data_analysis.md](docs/03_exploratory_data_analysis.md)

---

### 📄 Business Insights Documentation
This notebook provides actionable business insights derived from the ride cancellation data. It highlights key patterns, temporal trends, vehicle types, and payment methods affecting cancellations, along with recommendations for improving platform reliability, customer satisfaction, and driver efficiency.

You can view and run the notebook here:  
[04_business_insights.md](docs/04_business_insights.md)

---

### Key Analyses in the Notebook
- **Temporal Analysis:** Hourly, 15-minute intervals, day of month, day of week, and weekday vs weekend  
- **Categorical Feature Analysis:** Vehicle Type and Payment Method one-hot encoded features analyzed for cancellation trends  
- **Observations:** Peak cancellation times, high-risk vehicle types, and payment methods highlighted  

---

## Machine Learning Pipeline
The machine learning workflow is designed as a linear pipeline aligned with the weekly project plan. The pipeline includes the following stages:

1. Problem Definition & Business Understanding  
2. Data Loading  
3. Data Cleaning & Preprocessing  
4. Exploratory Data Analysis (EDA)  
5. Feature Engineering  
6. Model Training  
7. Model Evaluation  
8. Prediction  
9. Insight Generation  
10. Deployment and Demo Interface  

The complete workflow is illustrated using an activity diagram.

---

## Activity Diagram
The activity diagram illustrates the complete end-to-end machine learning pipeline, starting from business problem definition to model deployment and result visualization. The workflow is aligned with the weekly project plan and does not include decision nodes, as the process follows a linear pipeline structure.

The activity diagram is provided both as a visual image and as an editable draw.io source file in the `diagrams/` folder. A detailed textual explanation of the activity diagram is available in the file `ml_pipeline_activity_description.txt`.

---

## Project Structure
- data/ – Raw dataset  
- notebooks/ – Jupyter notebooks for each stage of the ML pipeline  
- models/ – Trained machine learning models  
- deployment/ – Demo application for model deployment  
- diagrams/ – UML activity diagram (PNG and draw.io source)  
- docs/ – Project management documentation (team members, timeline, budget)  
- ml_pipeline_activity_description.txt – Textual explanation of the ML pipeline  

---

## Dataset
- The raw dataset is stored in the `data/raw/` directory  
- The processed dataset is generated during the data cleaning and feature engineering steps  
- Due to file size limitations, processed data files are not stored in the repository and can be generated by running the notebooks  

---

## Technologies Used
- Python  
- Pandas, NumPy  
- Scikit-learn  
- Matplotlib, Seaborn  
- Streamlit or Flask  

---

## How to Run

1. Install the required libraries:

```bash
pip install -r requirements.txt
```
2. Run the notebooks in order from the notebooks/ folder to reproduce the machine learning pipeline.

## Deployment Status

This project has been successfully completed and fully deployed as a functional machine learning application.
The final version includes an end-to-end integration of the trained machine learning model within a user-friendly web interface. The system allows real-time prediction of ride cancellation probabilities based on user inputs and provides immediate, interpretable results.
The deployment demonstrates a complete production-like workflow, including data processing, model inference, and interactive visualization.

## Project Documentation
Project planning details such as team members, project overview, timeline, and budget are documented in the Excel file located in the docs/ folder.

## Author
Zehra Buse Tüfekçi
