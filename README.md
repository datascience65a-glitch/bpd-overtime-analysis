https://youtu.be/PPNYpHPYAgs
# Boston Police Department (BPD) Budget & Payroll Analysis  

## Project Overview  
This project analyzes the **Boston Police Department (BPD) budget and payroll data (2024)** to understand:   
- Shifts in funding across departments.  
- Officer pay trends (regular vs overtime pay).  
- Employees with highest regular pay with respect to other Boston city employees.  
- Prediction of overtime expenditure based on regular,retro,injure,other payments given to the employees using regression.

## Dataset and Dataset preprocessing 
The analysis uses single dataset:  
- **Employee Earnings Data (2024)** – Payroll data for all Boston employees (filter for police). This is the original dataset link: https://data.boston.gov/dataset/employee-earnings-report/resource/579a4be3-9ca7-4183-bc95-7d67ee715b6d. 
- **Cleaned_police_overtime_data**- The data that is filtered and cleaned with zero missing values.
**Dataset preprocessing**
  - The original dataset had many missing values. So at the first we removed the columns which had the most missing values compared to the values present or the columns that were redundant. Column - QUINN_EDUCATION, TOTAL GROSS were dropped.
  - Data was the preprocessed with filling of missing values using data augmentation tools like SimpleImputer, IterativeImputer
  - Dataset was then ready with 14057 data values and with zero missing values.

---
## Data Visualization
- Data will be visualized using the pie charts and the bar plots.
- Data that was preprocessed was visualized by seeing:
   - Distribution of regular pay for different departments with pie and bar plots.
   - Top 10 police employees by total pay using the bar plot
   - Relationship between Regular pay and overtime pay using the scatter plot
   - Correlation Heatmap among the pay components
   - Distribution of pay components (regular+injury+other+detail+overtime) using bar and pie plots
   
## Train/Test Strategy:
- Data will be split into 80-20 split. 80 percent of the data will be used as a training data and the later 20 percent would be used as a test data to check the performances of the models.
  
## Models:
Data was split into X and Y dataset. X columns represent the input(The numerical columns other than OVERTIME) and Y column represent the output(OVERTIME). Then models were used:
- XGBoost will be the main model to be used with results mean absolute error: $2756.10 and $r^2$ score = 0.820. Additionally, there are more models that are going to be used those are:
    - Random Forest Regressor with $R^2$ score = 0.813 and mean absolute error:$2838.64
   - Linear Regression with $R^2$ score = 0.709 and mean absolute error:$4420.76   
- There are shape value explainers also added to visualize which inputs are important thereby affecting the output.
Additionally clustering was done among officers using KMeans based on pay patterns . We have also summarized the clustering analysis.

## Codes:
- Boston_Police_Overtime.ipynb explains the data preprocessing and cleaning part. It also visualizes distribution of regular pay for different apartments using bar and pie plots.This code uses employee_earnings_report_2024.csv and creates cleaned_police_overtime_data.csv.
- data_visualization.ipynb explains the data visualization part of the project. This code uses cleaned_police_overtime_data.csv.
- ML_Model_DS_Project.ipynb explains the models part of the project. This code uses cleaned_police_overtime_data.csv.


## Goals achieved:  
- Shifts in funding across departments.  
- Officer pay trends (regular vs overtime pay).  
- Employees with highest regular pay with respect to other Boston city employees.  
- Prediction of overtime expenditure based on regular,retro,injure,other payments given to the employees by data preprocessing and using different models with results.
- Explored clustering of officers based on scatter plot of overtime pay vs regular pay.
   
## Future Extension Goals: 
- Predict future overtime costs using ML models.  
- Detect anomalies in officer pay patterns.   
- Investigate systemic trends or inequalities.
- Build classification models to predict which officers are likely to become “high overtime earners” in future years.  
---

## Tech Stack  
- **Python** (data preprocessing, ML models)  
- **Google Colab** (development environment, notebooks)  

---
