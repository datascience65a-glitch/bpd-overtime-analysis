# Boston Police Department (BPD) Budget & Payroll Analysis  

## Project Overview  
This project analyzes the **Boston Police Department (BPD) budget and payroll data (2024)** to understand:  
- Year-over-year changes in the BPD budget.  
- Shifts in funding across departments.  
- Officer pay trends (regular vs overtime vs injury pay).  
- Comparison of BPD pay with other Boston city employees.  
- Overtime trends and forecasting for the upcoming year.   

 **Extension Goals (if time permits):**  
- Predict future overtime costs using ML models.  
- Detect anomalies in officer pay patterns.  
- Explore clustering of officers based on pay/(Overtime)OT behavior.  
- Investigate systemic trends or inequalities.
- Build classification models to predict which officers are likely to become “high overtime earners” in future years.  
---

## Dataset  
The analysis uses multiple datasets:  
- **Employee Earnings Data (2024)** – Payroll data for all Boston employees (filter for police). This is the main dataset link is https://data.boston.gov/dataset/employee-earnings-report/resource/579a4be3-9ca7-4183-bc95-7d67ee715b6d. 
- **Overtime Data (2012–2022)** – Court, detail, and special event (Overtime)OT hours.  
- **BPD Roster** – Officer-level demographic info.  
- **City of Boston Operating Budget (2025)** – Budget allocations.  

---
## Data Visualization
- Data will be visualized using the pie charts and the bar plots and if time permits, we also plan to develop a dashboard with the help of tableau/power bi by the end of the semester.

## Train/Test Strategy:
- Data will be split into 80-20 split. 80 percent of the data will be used as a training data and the later 20 percent would be used as a test data to check the performances of the models.
  
##Models:
- XGBoost will be the main model to be used. Additionally, there are two more models that are going to be used those are:
- Random Forest
- ARIMA/HOLT-Winters(Data analytic model)(Datasets used would be from 2020-2024 for this model)
  <br/>Dataset for 2023:https://data.boston.gov/dataset/employee-earnings-report/resource/6b3c5333-1dcb-4b3d-9cd7-6a03fb526da7?inner_span=True
  <br/>Dataset for 2022:https://data.boston.gov/dataset/employee-earnings-report/resource/63ac638b-36c4-487d-9453-1d83eb5090d2?inner_span=True
  <br/>Dataset for 2021:https://data.boston.gov/dataset/employee-earnings-report/resource/ec5aaf93-1509-4641-9310-28e62e028457?inner_span=True
  <br/>Dataset for 2020:https://data.boston.gov/dataset/employee-earnings-report/resource/e2e2c23a-6fc7-4456-8751-5321d8aa869b?inner_span=True

## Tech Stack  
- **Python** (data preprocessing, ML models)  
- **Google Colab** (development environment, notebooks)  
- **Power BI** (interactive dashboards, visual storytelling)  
- **ArcGIS** (geospatial analysis – if applicable)  

---

