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
Employed for initial data exploration, cleaning, and validation. Excel facilitated quick checks on missing values, and descriptive statistics.

before importing the dataset into Power BI for advanced modeling.

## 🧮 DAX (Data Analysis Expressions)
Applied to create dynamic measures and KPIs such as churn rate, lost revenue, retention rate, and average tenure. DAX formulas ensured accurate calculations, enabled scenario analysis, and supported executive-level insights through custom logic.
---------------------------------------------------------------------------------------
# 4️⃣ Data Processing & Modeling

## 🧹 Data Cleaning and Remove Blank Values


## 🔄 Data Transformation
Created tenure buckets (0–12, 13–24, …, 60+ months) for churn trend analysis.

Derived churn KPIs (Churn Rate, Retention Rate, Lost Revenue).

Built calculated columns for segmentation (e.g., Partner/NoPartner, Dependents/NoDependents).

## 🧮 DAX Measures (KPI Formulas)

------------------------------------------------------------------------------------

# 5️⃣ Challenges & Solutions

## 🗂️ Data Issues
Missing values in TotalCharges required cleaning before analysis.

Overlapping categories (e.g., customers belonging to multiple churn drivers) led to percentages exceeding 100%.

Dataset provided as a single table without external validation or enrichment.

## ⚙️ Technical Challenges
More than 70 measures were created to capture different churn perspectives.

A major issue occurred when performing unpivot on service-related fields:

The process multiplied the number of rows by 6 (one for each service).

This caused incorrect duplication across all measures and KPIs.

As a result, churn rates and revenue impacts were inflated and inconsistent.

## 📊 Analytical Challenges
Ensuring that KPIs reflected realistic business logic despite overlapping categories.

Maintaining clarity in executive dashboards while handling complex customer attributes.

Balancing simplicity for decision-makers with technical accuracy in DAX formulas.

## ✅ Implemented Solutions
Rewrote all measures to avoid duplication and ensure correctness without relying on unpivoted service rows.

Applied controlled DAX logic to calculate churn rates, lost revenue, and retention KPIs directly from the base table.

Standardized terminology and visualization formats to maintain executive clarity.

Adopted a systems-thinking approach: fixing root causes in measures so corrections cascaded through all dependent KPIs.

--------------------------------------------------------------------

# 6️⃣ Statistics Overview

## 📊 Descriptive Statistics

Total Customers: 7,032

Churned Customers: 1,869 (≈26.6%)

Average Tenure: 32.42 months

Average Monthly Charges: $64.79

Total Lost Revenue: $2.86M (≈17.8% of total revenue) These descriptive figures provide a baseline understanding of churn magnitude and financial impact.

## 📈 Trend Analysis
Tenure vs. Churn: Churn rate decreases steadily as customer tenure increases.

Contract Type: Month-to-month contracts show the highest churn (42.7%), while two-year contracts show the lowest (2.85%).

Payment Method: Electronic check customers exhibit the highest churn (≈45%), while automatic bank transfer and credit card customers show much lower churn (≈15%).

## 📉 Distribution Analysis

- Demographics: Churn is evenly distributed across gender (≈51% male, 49% female).

- Senior Citizens: Higher churn rate (41.7%) compared to non-seniors (23.6%).

- Service Usage: Customers without added services (e.g., OnlineSecurity, TechSupport) show higher churn compared to those with bundled services.

## 📅 Seasonality

The dataset represents a static snapshot rather than time-series data across multiple years.

No seasonal patterns can be derived; however, tenure buckets provide a proxy for lifecycle stages, showing higher churn in early months and stability in later stages.
----------------------------------------------------------------------------------------------

## 📊 Tenure Statistics

| Measure              | Value        |
|----------------------|--------------|
| Mean                 | 32.42178612  |
| Standard Error       | 0.292703692  |
| Median               | 29           |
| Mode                 | 1            |
| Standard Deviation   | 24.54525971  |
| Sample Variance      | 602.4697742  |
| Kurtosis             | -1.38782258  |
| Skewness             | 0.237730832  |
| Range                | 71           |
| Minimum              | 1            |
| Maximum              | 72           |
| Sum                  | 227990       |
| Count                | 7032         |

---

## 💰 Monthly Charges Statistics

| Measure              | Value        |
|----------------------|--------------|
| Mean                 | 64.79820819  |
| Standard Error       | 0.358777041  |
| Median               | 70.35        |
| Mode                 | 20.05        |
| Standard Deviation   | 30.08597388  |
| Sample Variance      | 905.1658246  |
| Kurtosis             | -1.256156424 |
| Skewness             | -0.222102928 |
| Range                | 100.5        |
| Minimum              | 18.25        |
| Maximum              | 118.75       |
| Sum                  | 455661       |
| Count                | 7032         |

---

## 🧾 Total Charges Statistics

| Measure              | Value         |
|----------------------|---------------|
| Mean                 | 2283.300441   |
| Standard Error       | 27.03138426   |
| Median               | 1397.475      |
| Mode                 | 20.2          |
| Standard Deviation   | 2266.771362   |
| Sample Variance      | 5138252.407   |
| Kurtosis             | -0.231798761  |
| Skewness             | 0.9616425     |
| Range                | 8666          |
| Minimum              | 18.8          |
| Maximum              | 8684.8        |
| Sum                  | 16056168.7    |
| Count                | 7032          |
