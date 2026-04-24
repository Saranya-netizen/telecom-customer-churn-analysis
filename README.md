# 📊 Telecom Customer Churn Analysis & Prediction

## 🚀 Project Overview
This project focuses on analyzing customer behavior in the telecommunications industry to identify factors contributing to customer churn. By leveraging data cleaning techniques in Excel/Power Query and advanced data modeling in Power BI, I developed an interactive dashboard to visualize churn drivers and provide actionable retention strategies.

## 🎯 Project Objectives
* **Demonstrate Data Pre-processing:** Clean and transform raw telecom data for analysis.
* **Visualize Key Drivers:** Build an interactive Power BI dashboard to identify why customers leave.
* **Strategic Insight:** Provide actionable recommendations to reduce churn and increase Customer Lifetime Value (CLV).

## 🛠 Tools & Technologies
* **Data Cleaning:** Excel, Power Query
* **Visualization & Modeling:** Power BI
* **Language:** DAX (Data Analysis Expressions)

## 🏗 Data Workflow & Modeling
### Data Pre-Processing
* **Imputation:** Handled missing values in `Total Charges` using logical imputation to maintain data integrity.
* **Transformation:** Standardized categorical data (e.g., ensuring 'Yes'/'No' consistency), converted data types, and created custom metrics like `Tenure Bucket`, `Charge Bucket`, and `Senior Citizen Status`.
* **Modeling:** Transformed the flat dataset into a **Star Schema** with Fact and Dimension tables (Customer, Internet Connection, Service Type) linked via `Customer ID` using 1:1 relationships.

### Key DAX Measures
* **Churn Rate:** `DIVIDE(CALCULATE(COUNTROWS('Table'), 'Table'[Churn Status] = "Yes"), COUNTROWS('Table'))`
* **Total Revenue Lost:** `CALCULATE(SUM('Financial Data'[Total Charges]), 'Customer Data'[Customer Status] = "Churned")`
* **Average Tenure (Retained):** `CALCULATE(AVERAGE('Telecom Connection'[Tenure in Months]), 'Customer'[Customer Status] ="Stayed")`

## 📊 Key Findings & Insights
*Based on an analysis of 1,000 subscribers (26.58% Churn Rate):*

* **Customer Demographics:** Higher churn risk is observed among younger, single demographics (74.5% of churned customers are not senior citizens; 64.2% have no partner).
* **Customer Tenure:** Nearly 50% of churned customers were "new" (less than 10 months with the company).
* **Service Usage:** Fiber Optic users show the highest volume of churn.
* **Billing & Contract:** Month-to-month contracts are the highest risk segment; 75% of churned customers utilized paperless billing.

## 💡 Strategic Recommendations
* **Prioritize New Clients:** Implement "onboarding" retention offers/campaigns for customers in their first 10 months.
* **Contract Upselling:** Incentivize the transition from Month-to-Month contracts to 1 or 2-year terms.
* **Service Quality:** Investigate Fiber Optic service issues to mitigate dissatisfaction.
* **Value-Add Services:** Increase loyalty by bundling Online Security and other services for high-risk customer segments.
