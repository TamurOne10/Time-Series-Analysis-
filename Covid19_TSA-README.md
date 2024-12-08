COVID-19 Dataset Forecasting Model.
Overview
This project focuses on analyzing and forecasting COVID-19 trends in Pakistan using a dataset containing information about daily cases, deaths, recoveries, and travel history. Exploratory Data Analysis (EDA) is performed to uncover patterns and relationships between different features, followed by the implementation of a forecasting model using Prophet.
Dataset
The dataset contains daily records of COVID-19 cases in Pakistan from February 2020 to May 2020. It includes the following columns:
•	Date: The date of record.
•	Cases: Number of new COVID-19 cases reported.
•	Deaths: Number of deaths reported.
•	Recovered: Number of recoveries reported.
•	Travel_history: Source of exposure to COVID-19.
•	Province: The province where the cases were recorded.
•	City: The city where the cases were recorded.
Key Features of the Project
•	Data Cleaning and Preprocessing: Checked for null values, duplicates, and data inconsistencies. Standardized spelling errors in cities' names. Removed duplicate rows from the dataset.
•	Exploratory Data Analysis (EDA): Visualized trends using matplotlib, seaborn, and plotly. Analyzed relationships between variables like deaths, cases, and recoveries across provinces and cities.
•	Feature Engineering: Added a new column Active_Cases calculated as: Active_Cases = Cases - Recovered - Deaths.
•	Visualization: Time-series plots for daily cases, recoveries, and deaths. Bar charts comparing cases and deaths across provinces.
•	Forecasting: Implemented the Prophet library to predict COVID-19 active cases for 30 days into the future. Compared actual and predicted cases using plotly.
Libraries Used
pandas, numpy, matplotlib, seaborn, plotly, Prophet
How to Use
1. Clone the repository:
   git clone <repository-url>

2. Install the required dependencies:
   pip install -r requirements.txt

3. Run the Jupyter Notebook to analyze the dataset and visualize results.
Results
Daily trends for COVID-19 cases, recoveries, and deaths were analyzed. The forecasting model provides an accurate prediction of active cases for future periods.
Future Improvements
•	Expand the dataset to include more recent data.
•	Integrate additional features such as demographic and mobility data for deeper analysis.
•	Enhance the model's performance with hyperparameter tuning and alternative algorithms.
Contact Information
Author: Tamoor Abbas
Email: Tamur110@gmail.com

