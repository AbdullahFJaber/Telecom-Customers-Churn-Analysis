# Telecom-Customers-Churn-Analysis
Customer-Churn-Analysis is a Power BI project focused on analyzing customer churn in telecom services. It explores key drivers of churn, KPIs, and financial impacts through interactive dashboards, descriptive statistics, and executive-ready insights to support retention strategies, decision-making, and future optimization.

---------------------------------------------------------------------------

# 1️⃣ Project Overview


## 🎯 Project Objectives
The project aims to analyze customer churn patterns in telecom services, identify the top drivers of churn, and provide actionable insights through interactive dashboards. The ultimate goal is to support decision-makers in reducing churn and improving customer retention.

## 💡 Business Need
High churn rates directly impact revenue and customer lifetime value. Understanding why customers leave enables the business to design targeted retention strategies, optimize service offerings, and improve overall customer satisfaction.

## 👥 Stakeholders & Decisions
- Executive Management: Strategic decisions on retention investments.

- Customer Service Teams: Operational actions to address churn drivers.

- Data Analysts: Continuous monitoring and reporting of churn KPIs.

- Finance Department: Assessing financial impact of churn and retention initiatives.

## 📊 Scope & KPIs
The analysis covers customer demographics, contract types, payment methods, and service usage. Key KPIs include:

- Churn Rate 

- Churned Customers

- Lost Revenue

- Retention Rate 

- Average Tenure 

## ⚖️ Constraints & Data Realism
Dataset reflects telecom customer records with realistic attributes but limited external factors.

Some measures are aggregated, which may reduce interactivity between visuals.

Customers may belong to multiple categories, leading to overlapping churn drivers.

## ✅ Success Criteria
Deliver an executive-ready dashboard with clear explanatory text.

Highlight top churn drivers in descending order of risk.

Provide actionable insights that guide retention strategies.

Ensure clarity, realism, and usability for decision-makers.

----------------------------------------------------------------------------------------

# 2️⃣ Dataset Description 

## 🌐 Data Sources
The dataset is sourced from Kaggle Telecom Churn Dataset. It contains customer-level information including demographics, service subscriptions, contract types, payment methods, and churn status.

https://www.kaggle.com/datasets/pratap684/telecom-churn-dataset

## 🔗 Tables & Relationships
Single main table: Telecom Customers

Key field: customerID (unique identifier for each customer)

Relationships:

customerID links all attributes together.

No external tables are provided; relationships are implicit within the dataset.

Modeling: Converted into a Star Schema in Power BI with supporting calculated tables for segmentation and KPIs.

## 📖 Data Dictionary
Key fields include:

customerID → Unique customer identifier

gender → Male / Female

SeniorCitizen → Binary flag (0 = No, 1 = Yes)

Partner / Dependents → Yes / No

Tenure → Number of months the customer has stayed

PhoneService / MultipleLines → Yes / No / No phone service

InternetService → DSL / Fiber optic / No

OnlineSecurity / OnlineBackup / DeviceProtection / TechSupport / StreamingTV / StreamingMovies → Yes / No / No internet service

Contract → Month-to-month / One year / Two year

PaperlessBilling → Yes / No

PaymentMethod → Electronic check / Mailed check / Bank transfer (automatic) / Credit card (automatic)

MonthlyCharges → Numeric value of monthly fee

TotalCharges → Numeric value of total fee

Churn → Yes / No (target variable)

## ⚠️ Data Limitations
Single source dataset: No external validation or enrichment.

Synthetic realism: While realistic, the dataset may not fully represent actual telecom operations.

Overlapping categories: Customers may belong to multiple churn drivers, leading to percentages exceeding 100%.

Missing values: Some fields (e.g., TotalCharges) contain blanks requiring cleaning.

Static snapshot: Dataset represents a single time period, limiting trend analysis across multiple years.


-------------------------------------------------------------------------------------------------

# 3️⃣ Tools & Technologies

## 📊 Power BI
Used as the primary visualization and reporting tool. It enables interactive dashboards, KPI cards, slicers, and executive-ready summaries. Power BI also supports advanced modeling through relationships, star schema design, and custom visuals for churn analysis.

## 📑 Excel
Employed for initial data exploration, cleaning, and validation. Excel facilitated quick checks on missing values, descriptive statistics, and preliminary pivot tables before importing the dataset into Power BI for advanced modeling.

## 🧮 DAX (Data Analysis Expressions)
Applied to create dynamic measures and KPIs such as churn rate, lost revenue, retention rate, and average tenure. DAX formulas ensured accurate calculations, enabled scenario analysis, and supported executive-level insights through custom logic.
