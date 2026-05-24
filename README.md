Fraud Detection Machine Learning Project
<br>
This project focuses on identifying fraudulent financial transactions using a Machine Learning model and deploying it through a Streamlit web application. The model achieves approximately 94% accuracy in detecting fraud within a dataset of over 6 million records.<br>
Project Overview<br>
The goal of this project is to create an end-to-end data science solution that includes:<br>
Data Analysis & Visualization: Exploring transaction types, fraud rates, and account balance anomalies.<br>
Machine Learning Modeling: Building a classification pipeline to predict fraudulent activities.<br>
Web Deployment: A user-friendly Streamlit interface for real-time fraud prediction.<br>
Dataset<br>
The dataset used is a comprehensive fraud detection dataset from Kaggle, containing over 6.3 million rows and 11 columns. Key features include:<br>
Type: Transaction types (Cash-out, Transfer, Payment, etc.).<br>
Amount: The value of the transaction.<br>
Old/New Balance: Balance details for both the sender and receiver.<br>
isFraud: The target variable indicating whether a transaction was fraudulent.<br>
Note: The dataset exhibits a significant class imbalance, with fraud representing only 0.13% of the total data.<br>
Technologies Used<br>
Language: Python 3.11.4<br>
Data Manipulation: Pandas, NumPy<br>
Visualization: Matplotlib, Seaborn<br>
Machine Learning: Scikit-learn (Logistic Regression, Pipelines, Column Transformers)<br>
Model Export: Joblib<br>
Deployment: Streamlit<br>
Project Workflow<br>
Exploratory Data Analysis (EDA): Visualised fraud distribution and found that fraud occurs almost exclusively in 'Transfer' and 'Cash Out' transaction types.<br>
Feature Engineering: Dropped irrelevant columns (e.g., step, nameOrig, nameDest) and handled class imbalance using the balanced class weight parameter in Logistic Regression.<br>
Pipeline Creation: Developed a robust pipeline that includes StandardScaler for numerical data and OneHotEncoder for categorical data.<br>
Model Evaluation: Evaluated performance using classification reports and confusion matrices, focusing on the model's ability to catch fraud despite the imbalanced nature of the data.<br>
Deployment: Exported the trained pipeline as a .pickle file and integrated it into a Streamlit app.<br>
How to Run the Project<br>
Prerequisites<br>
Ensure you have the required libraries installed:<br>
pip install pandas numpy matplotlib seaborn scikit-learn streamlit joblib<br>
Running the Web App<br>
Download the Kaggle dataset and ensure the processed model (fraud_detection_pipeline.pickle) is in your directory.<br>
Run the following command in your terminal:<br>
streamlit run fraud_detection.py<br>
Open the local URL provided by Streamlit in your browser.<br>
App Features<br>
The Streamlit app allows users to input transaction details such as:<br>
Transaction Type (Select box)<br>
Amount<br>
Sender/Receiver Balances<br>
The app then uses the pre-trained model to provide an instant prediction: "This transaction can be fraud" or "This transaction looks like it is not a fraud"<br>
