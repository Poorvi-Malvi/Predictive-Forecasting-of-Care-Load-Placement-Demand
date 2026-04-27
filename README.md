# Predictive-Forecasting-of-Care-Load-Placement-Demand
Predictive analytics dashboard for forecasting care load and placement demand using time-series analysis and scenario-based modeling. Built with Python and Streamlit to support proactive capacity planning and decision-making.


**📊 Predictive Forecasting of Care Load & Placement Demand**

🧠 Project Overview

This project focuses on building a predictive analytics system for forecasting the number of children in care within the U.S. HHS Unaccompanied Alien Children (UAC) Program.

The system transforms historical operational data into forward-looking intelligence to support proactive decision-making in resource allocation, capacity planning, and humanitarian response.

Instead of only analyzing past trends, this project enables short-term forecasting of care load and discharge demand, helping identify potential system stress in advance.

*🎯 Objectives*

Primary Objectives:

Forecast the number of children under HHS care
Predict short-term placement (discharge) demand
Estimate system load under different future scenarios

Secondary Objectives:

Identify pressure points between intake and discharge flow
Build early-warning indicators for capacity stress
Compare baseline statistical and trend-based forecasting approaches

*📁 Dataset Description*

The dataset contains daily operational metrics:

Column	                                  Description
Date	                                    Reporting date
Children in HHS Care                    	Active care load
Children in CBP custody	                  Initial custody count
Children transferred out of CBP custody	  Flow into HHS system
Children discharged from HHS Care	        Successful placements
Children apprehended	                    Intake volume

*⚙️ Methodology*

1. Data Preprocessing

Converted date column to datetime format
Handled missing values using forward/backward fill
Removed inconsistencies and non-numeric formatting (e.g., commas in numbers)
Created synthetic time index where required

2. Feature Engineering
   
Lag features (t-1, t-7, t-14)
Rolling averages (7-day, 14-day)
Rolling standard deviation for volatility
Flow-based pressure indicator:
Transfers − Discharges
Calendar-based features (day, month)

3. Forecasting Approach
   
Trend-based forecasting model
Scenario-based adjustments:
Normal conditions
High intake surge
Low discharge scenario

4. Evaluation Metrics
 
MAE (Mean Absolute Error)
RMSE (Root Mean Squared Error)
MAPE (Mean Absolute Percentage Error)
Capacity Breach Probability


*📊 Key Performance Indicators (KPIs)*

Forecast Accuracy (%) → reliability of predictions
System Pressure Index → imbalance between inflow and outflow
Capacity Breach Risk (%) → probability of exceeding threshold
Average Care Load → baseline operational load

*🖥️ Streamlit Dashboard Features*

*📈 Forecast Module*

Future care load prediction
Scenario-based simulation
Trend visualization

*📊 System Analysis*

Discharge trends
Pressure indicator visualization
Historical pattern tracking

*🧠 Insights Panel*

Automated operational insights
KPI summary dashboard
Risk interpretation

*⚙️ Interactive Controls*

Forecast horizon selector (7–30 days)
Scenario selection (Normal / Surge / Delay)

*🧪 Technologies Used*

Python
Pandas
NumPy
Matplotlib
Streamlit
Statsmodels (ARIMA - optional experimentation)

*📌 Key Insights from Analysis*

Care load follows strong temporal dependency patterns
System pressure helps identify early stress signals
Forecasting enables proactive capacity planning
Scenario simulation improves operational preparedness

*📈 Future Improvements*

Integrate ML models (Random Forest, Gradient Boosting)
Add real-time data pipeline
Deploy dashboard on cloud (Streamlit Cloud / AWS)
Add alert system for capacity breach warnings
Improve probabilistic forecasting with confidence intervals

*👨‍💻 Author*

Poorvi Malvi
B.Tech CSE (Data Science & Engineering)
Aspiring Data Analyst | ML & Analytics Enthusiast
