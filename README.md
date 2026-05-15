# Ride Cancellation Prediction – Machine Learning Project

## Project Overview
This project aims to predict the probability of ride cancellations using machine learning techniques. It follows an end-to-end ML pipeline covering business understanding, data preparation, feature engineering, model development, and deployment. The goal is to support operational decision-making by identifying potential ride cancellations in advance and improving service efficiency.

## Business Problem
Ride cancellations negatively impact customer satisfaction and operational efficiency. Predicting cancellations in advance enables proactive interventions such as better driver allocation, improved scheduling, and reduced operational loss.

## Business Objectives
Detailed documentation:
- 📄 [Business Objectives](docs/business_objectives.md)
- 📊 [Business Value & Success Metrics](docs/business_value_and_metrics.md)

## Data Preparation & Feature Engineering
- 📄 [Data Cleaning](docs/01_cleaning_documentation.md)
- 📄 [Feature Engineering](docs/02_feature_engineering_documentation.md)
- 📄 [Exploratory Data Analysis](docs/03_exploratory_data_analysis.md)
- 📄 [Business Insights](docs/04_business_insights.md)

## Machine Learning Pipeline
The project follows a structured end-to-end ML pipeline: Business Understanding, Data Collection, Data Cleaning & Preprocessing, Exploratory Data Analysis (EDA), Feature Engineering, Model Training, Model Evaluation, Prediction, Insight Generation, and Deployment.

## Project Structure
data/ – Raw and processed datasets  
notebooks/ – ML pipeline notebooks  
models/ – Trained machine learning models  
deployment/ – Streamlit application  
diagrams/ – Architecture and pipeline diagrams  
docs/ – Project documentation  

## Dataset
Raw data is stored in data/raw/. Processed data is generated during preprocessing steps. Large intermediate files are excluded due to GitHub size limitations and can be reproduced by running the notebooks.

## Technologies Used
Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Streamlit

## Deployment
The project has been successfully deployed as a fully functional web application using Streamlit. The application provides a user input-based prediction system, real-time cancellation probability output, interactive interface, and end-to-end integration of the trained machine learning model. It represents a complete real-world simulation of a ride cancellation prediction system.

## How to Run Locally
pip install -r requirements.txt  
Run notebooks in order from the notebooks/ folder  
streamlit run deployment/app.py  

## Project Status
Completed – End-to-end machine learning project successfully implemented and deployed.

## Author
Zehra Buse Tüfekçi
