# Boston Police Department (BPD) Budget & Payroll Analysis  

## Project Overview  
This project analyzes the **Boston Police Department (BPD) budget and payroll data (2024)** to understand:   
- Shifts in funding across departments.  
- Officer pay trends (regular vs overtime vs injury pay).  
- Employees with highest regular pay with respect to other Boston city employees.  
- Prediction of overtime expenditure based on regular,retro,injure,other payments given to the employees.

 **Extension Goals (if time permits):**  
- Predict future overtime costs using ML models.  
- Detect anomalies in officer pay patterns.  
- Explore clustering of officers based on pay/(Overtime)OT behavior.  
- Investigate systemic trends or inequalities.
- Build classification models to predict which officers are likely to become “high overtime earners” in future years.  
---

## Dataset and Dataset preprocessin 
The analysis uses multiple datasets:  
- **Employee Earnings Data (2024)** – Payroll data for all Boston employees (filter for police). This is the original dataset link is https://data.boston.gov/dataset/employee-earnings-report/resource/579a4be3-9ca7-4183-bc95-7d67ee715b6d. 
- **Cleaned_police_overtime_data**- The data that is filtered and cleaned with zero missing values.
**Dataset preprocessing**
  - The original dataset had many missing values. So at the first we removed the columns which had the most missing values compared to the values present or the columns that were redundant. Column - QUINN_EDUCATION, TOTAL GROSS were dropped.
  - Data was the preprocessed with filling of missing values using data augmentation tools like SimpleImputer, IterativeImputer
  - Dataset was then ready with 14057 data value with zero missing values.

---
## Data Visualization
- Data will be visualized using the pie charts and the bar plots.
- Data that was preprocessed was visualized by seeing:
   - Top 10 police employees by total pay using the bar plot
   - Relationship between Regular pay and overtime pay using the scatter plot
   - Correlation Heatmap between the pay components
   - Distribution of pay components using bar and pie plots
   - Distribution of regular pay for different departments with pie and bar plots.

## Train/Test Strategy:
- Data will be split into 80-20 split. 80 percent of the data will be used as a training data and the later 20 percent would be used as a test data to check the performances of the models.
  
##Models:
- XGBoost will be the main model to be used with results mean absolute error: $2756.10 and r^2 score = 0.820. Additionally, there are more models that are going to be used those are:
- Random Forest Regressor
-Linear Regression 

## Tech Stack  
- **Python** (data preprocessing, ML models)  
- **Google Colab** (development environment, notebooks)  
- **Power BI** (interactive dashboards, visual storytelling)  
- **ArcGIS** (geospatial analysis – if applicable)  

---
