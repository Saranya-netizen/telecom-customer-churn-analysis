Telecom Customer Churn Analysis & Prediction
🚀 Project Overview
This project focuses on analyzing customer behavior in the telecommunications industry to identify factors contributing to customer churn. By leveraging data cleaning techniques in Excel/Power Query and advanced data modeling in Power BI, I developed an interactive dashboard to visualize churn drivers and provide actionable retention strategies.

🎯 Objective
Demonstrate Data Pre-processing: Clean and transform raw telecom data.

Visualize Key Drivers: Build an interactive Power BI dashboard to identify why customers leave.

Strategic Insight: Provide actionable recommendations to reduce churn and increase Customer Lifetime Value (CLV).

🛠 Tools & Technologies
Data Cleaning: Excel, Power Query

Visualization & Modeling: Power BI

Language: DAX (Data Analysis Expressions)

🏗 Data Workflow & Modeling
Data Pre-Processing
Imputation: Handled missing values in Total Charges using logical imputation.

Transformation: Standardized categorical data (e.g., Yes/No consistency), converted data types, and created custom buckets (Tenure Bucket, Charge Bucket, Senior Citizen Status).

Modeling: Transformed the flat dataset into a Star Schema with Fact and Dimension tables (Customer Table, Internet Connection Table, Service Type Table) linked via Customer ID with a 1:1 relationship.

Key DAX Measures
Some of the core calculations used to derive insights:

Code snippet
Churn Rate = DIVIDE(CALCULATE(COUNTROWS('Table'), 'Table'[Churn Status] = "Yes"), COUNTROWS('Table'))

Total Revenue Lost = CALCULATE(SUM('Financial Data'[Total Charges]), 'Customer Data'[Customer Status] = "Churned")

Average Tenure of Retained = CALCULATE(AVERAGE('Telecom Connection'[Tenure in Months]), 'Customer'[Customer Status] ="Stayed")
📊 Key Findings & Insights
Based on the analysis of 1,000 subscribers (26.58% Churn Rate):

Customer Demographics: 74.5% of churned customers are not senior citizens, and 64.2% of churned customers had no partner. This indicates higher churn risk among younger, single demographics.

Customer Tenure: Nearly 50% of churned customers were "new" (less than 10 months with the company), highlighting an immediate need to focus on early-stage retention.

Service Usage: Fiber Optic users show the highest churn volume.

Billing & Contract: Month-to-month contracts are the highest risk segment. 75% of churned customers utilized paperless billing.

💡 Strategic Recommendations
Based on the predictive analysis, the company should:

Prioritize New Clients: Implement "onboarding" retention offers for customers in their first 10 months.

Contract Upselling: Incentivize the move from Month-to-Month contracts to 1 or 2-year terms.

Service Quality: Investigate Fiber Optic service issues, as this segment exhibits high dissatisfaction.

Value-Add: Improve loyalty by bundling Online Security and other value-added services for high-risk segments.
