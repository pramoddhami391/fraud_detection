<b>Fraud Detection Machine Learning ProjectFraud Detection Machine Learning Project<b>
This project focuses on identifying fraudulent financial transactions using a Machine Learning model and deploying it through a Streamlit web application. The model achieves approximately 94% accuracy in detecting fraud within a dataset of over 6 million records.
Project Overview
The goal of this project is to create an end-to-end data science solution that includes:
Data Analysis & Visualization: Exploring transaction types, fraud rates, and account balance anomalies.
Machine Learning Modeling: Building a classification pipeline to predict fraudulent activities.
Web Deployment: A user-friendly Streamlit interface for real-time fraud prediction.
Dataset
The dataset used is a comprehensive fraud detection dataset from Kaggle, containing over 6.3 million rows and 11 columns. Key features include:
Type: Transaction types (Cash-out, Transfer, Payment, etc.).
Amount: The value of the transaction.
Old/New Balance: Balance details for both the sender and receiver.
isFraud: The target variable indicating whether a transaction was fraudulent.
Note: The dataset exhibits a significant class imbalance, with fraud representing only 0.13% of the total data.
Technologies Used
Language: Python 3.11.4
Data Manipulation: Pandas, NumPy
Visualization: Matplotlib, Seaborn
Machine Learning: Scikit-learn (Logistic Regression, Pipelines, Column Transformers)
Model Export: Joblib
Deployment: Streamlit
Project Workflow
Exploratory Data Analysis (EDA): Visualised fraud distribution and found that fraud occurs almost exclusively in 'Transfer' and 'Cash Out' transaction types.
Feature Engineering: Dropped irrelevant columns (e.g., step, nameOrig, nameDest) and handled class imbalance using the balanced class weight parameter in Logistic Regression.
Pipeline Creation: Developed a robust pipeline that includes StandardScaler for numerical data and OneHotEncoder for categorical data.
Model Evaluation: Evaluated performance using classification reports and confusion matrices, focusing on the model's ability to catch fraud despite the imbalanced nature of the data.
Deployment: Exported the trained pipeline as a .pickle file and integrated it into a Streamlit app.
How to Run the Project
Prerequisites
Ensure you have the required libraries installed:
pip install pandas numpy matplotlib seaborn scikit-learn streamlit joblib
Running the Web App
Download the Kaggle dataset and ensure the processed model (fraud_detection_pipeline.pickle) is in your directory.
Run the following command in your terminal:
streamlit run fraud_detection.py
Open the local URL provided by Streamlit in your browser.
App Features
The Streamlit app allows users to input transaction details such as:
Transaction Type (Select box)
Amount
Sender/Receiver Balances
The app then uses the pre-trained model to provide an instant prediction: "This transaction can be fraud" or "This transaction looks like it is not a fraud"
