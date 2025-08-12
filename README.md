US Flight Delay Analysis
Trends, Root Causes, and Predictive Modeling

** Overview**
This project analyzes historical US flight delay data to identify key trends, understand root causes, and develop predictive models for both classification (will a flight be delayed?) and regression (how long will the delay be?).

By combining data analytics, machine learning, and explainable AI (OAI + SHAP), the project aims to help airlines make smarter operational decisions and reduce controllable delays.

 ** Key Insights**
Most frequent delay causes: Late Aircraft & Carrier Delays (both controllable by airlines)

Hard-to-control delays: NAS (air traffic congestion), Weather

Least significant delay cause: Security delays

Best month for on-time performance: February

 ** Models Used
Classification: Random Forest + SMOTE
Goal: Predict whether a flight will be delayed

Accuracy: 63%

ROC AUC: 0.67

F1 (Delayed Class): 0.54

Regression: Random Forest Regressor
Goal: Predict delay duration (minutes)

MAE: ~21.1 minutes

RMSE: ~38.5 minutes

** Why Random Forest?
Handles non-linear interactions and mixed feature types

Resistant to overfitting via ensemble learning

Provides feature importance for explainability

Works well with imbalanced and noisy operational data


** Operational Adjustability Index (OAI)
To prioritize actionable delay causes, features were assigned an adjustability score:

1 = Fully controllable (e.g., carrier scheduling)

0.5 = Partially controllable (e.g., airport congestion)

0 = Not controllable (e.g., time of year)

OAI = Feature Importance × Adjustability Score


** Recommendations
Operational: Introduce buffer time, improve crew & aircraft turnaround

Weather: Use ML to forecast high-risk periods

Airspace: Strengthen ATC & FAA coordination

Carrier-Level: Optimize scheduling for carriers with high delay ratios


** Dataset
Source: Historical US Flight Data (2015–2024)
Includes:

Delay counts & causes

Flight cancellations/diversions

Categorical data (carrier, airport, month, year)





