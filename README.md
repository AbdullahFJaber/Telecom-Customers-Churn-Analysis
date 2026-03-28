# Telecom-Customers-Churn-Analysis
Customer-Churn-Analysis is a Power BI project focused on analyzing customer churn in telecom services. It explores key drivers of churn, KPIs, and financial impacts through interactive dashboards, descriptive statistics, and executive-ready insights to support retention strategies, decision-making, and future optimization.

---------------------------------------------------------------------------

# 1️⃣ Project Overview


## 🎯 Project Objectives
The project aims to analyze customer churn patterns in telecom services, identify the top drivers of churn, and provide actionable insights through interactive dashboards. The ultimate goal is to support decision-makers in reducing churn and improving customer retention.

## 📖 Case Study Scenario
Provide a real-world scenario illustrating how churn analysis impacts telecom decision-making.

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

## 📊 Dashboard Preview

<img width="982" height="553" alt="CustomerOverview" src="https://github.com/user-attachments/assets/20b60b8d-58cc-4758-a1d5-aa0372c76072" />

----------------------------------------------------------------------------------------

<img width="982" height="549" alt="Services Products" src="https://github.com/user-attachments/assets/0273f03e-be64-4e1c-aedf-efdd7c463667" />

----------------------------------------------------------------------------------------

<img width="981" height="548" alt="Contracts Payment" src="https://github.com/user-attachments/assets/968533c1-5e84-4077-95b1-600ec624e214" />

----------------------------------------------------------------------------------------

<img width="984" height="557" alt="Churn Analysis" src="https://github.com/user-attachments/assets/1ed1c6a8-c1b6-4d36-be40-d475c8aa2454" />

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

## 🧮 DAX 

Data Analysis Expressions Applied to create dynamic measures and KPIs such as churn rate, lost revenue, retention rate, and average tenure. DAX formulas ensured accurate calculations, enabled scenario analysis, and supported executive-level insights through custom logic.


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

------------------------------------------------------------------------------------

## 7️⃣ Insight Summaries

- Short-term contracts and manual payment methods are the strongest churn drivers.

- Senior customers and those lacking additional services are more likely to leave.

- Retention strategies should prioritize converting month-to-month contracts into longer terms, promoting secure automatic payments, and bundling services to increase customer stickiness.

----------------------------------------------------------------------------------------

# 8️⃣ Indicators Linkage

## 🔗 KPI Dependencies
Churn Rate (%) depends on the count of churned customers relative to total customers.

Lost Revenue ($) depends on monthly charges of churned customers.

Retention Rate (%) is the inverse of churn rate, directly linked to customer loyalty.

Average Tenure depends on customer lifecycle duration and influences churn probability.

## ⚡ Cause–Effect Relationships
Short-term contracts → Higher churn → Increased lost revenue.

Electronic check payments → Higher churn → Lower retention.

Lack of value-added services → Higher churn → Reduced customer lifetime value.

Senior citizen segment → Higher churn → Greater vulnerability in customer base.

## 🔄 Cross-Metric Correlations
Churn Rate vs. Lost Revenue: Direct positive correlation; higher churn increases financial loss.

Tenure vs. Churn Rate: Negative correlation; longer tenure reduces churn likelihood.

Payment Method vs. Retention Rate: Automatic payments correlate with higher retention.

Service Bundling vs. Customer Lifetime Value: More services lead to lower churn and higher revenue stability.

## 💰📈 Financial / Operational / Quality Indicators
Financial: Lost Revenue, Lost Revenue %, Average Monthly Charges.

Operational: Contract Type distribution, Payment Method adoption, Service usage patterns.

Quality: Customer satisfaction proxies (e.g., TechSupport, OnlineSecurity usage) linked to churn reduction.

-----------------------------------------------------------------------------

# 9️⃣ Root Cause Analysis

## 🪢 Identified Root Causes
Short-term contracts (Month-to-month): Strongest driver of churn, with rates exceeding 42%.

Electronic check payments: Associated with the highest churn rate (≈45%), indicating risk in manual payment methods.

Lack of value-added services: Customers without OnlineSecurity, TechSupport, or DeviceProtection churn at significantly higher rates.

Senior citizen segment: Higher churn (≈41.7%) compared to non-seniors, reflecting demographic vulnerability.

## 🔍 Drill-down Findings
Customers with multiple risk factors combined (e.g., month-to-month + electronic check + no added services) show compounded churn risk.

Tenure buckets reveal that churn is concentrated in the first 12 months, declining steadily afterward.

Service adoption analysis shows that bundled services reduce churn likelihood across all demographics.


## 📑 Supporting Evidence
Dashboard visuals: Churn by contract, payment method, and service usage consistently highlight the same top drivers.

Descriptive statistics: Confirmed concentration of churn in early tenure and among specific payment methods.

DAX measures: Validated churn KPIs after correcting duplication errors caused by unpivoting services.

Cross-metric correlations: Strong positive link between churn rate and lost revenue, reinforcing financial impact.

----------------------------------------------------------------------------------------------------------------

# 🔟 Quantitative Impact

## 💰 Financial Impact
Total Lost Revenue: ≈ $2.86M due to churned customers.

Monthly Lost Revenue: ≈ $139K recurring loss.

Lost Revenue %: ≈ 17.8% of total revenue base. 👉 Churn directly erodes profitability and long-term financial stability.

## 📉 Revenue Impact
Churn Rate: 26.6% of customers left the service.

High-risk segments: Month-to-month contracts and electronic check payments account for the majority of lost revenue.

Retention opportunity: Converting vulnerable segments to long-term contracts could recover millions in annual revenue.

## 💸 Cost Impact
Increased customer acquisition costs to replace churned customers.

Higher support costs for dissatisfied customers prior to churn.

Reduced economies of scale as churn decreases the active customer base.

## ⚙️ Efficiency Impact
Operational inefficiency: Resources spent on onboarding churned customers yield no long-term value.

Service adoption gap: Customers without bundled services churn faster, reducing efficiency of service delivery.

Retention programs: Targeted interventions improve efficiency by focusing on high-risk segments instead of broad campaigns.

## 🔄 Before vs. After Comparison

- Before (Baseline): High churn rate (26.6%), significant lost revenue ($2.86M), weak retention among short-term contracts.

- After (Proposed Strategy):

Reduced churn through contract upgrades and automatic payment adoption.

Improved retention rate, lowering lost revenue percentage.

Increased efficiency by aligning services with customer needs. 👉 The comparison highlights measurable gains in financial recovery, operational efficiency, and customer loyalty.

--------------------------------------------------------------------------

# 1️⃣1️⃣ Executive Summary

<img width="975" height="553" alt="Top Churn Drivers" src="https://github.com/user-attachments/assets/b5fced93-0a91-4f15-ac40-9483fac43b56" />

--------------------------------------------------------------------------

## 📊 High-level Findings
Overall churn rate is 26.6%, representing a significant risk to revenue.

Month-to-month contracts and electronic check payments are the strongest churn drivers.

Senior citizens and customers without value-added services (e.g., OnlineSecurity, TechSupport) show higher churn.

Retention strategies can recover millions in lost revenue annually.

## ⚠️ Major Risks
Revenue erosion: $2.86M lost due to churned customers.

Customer vulnerability: High churn in early tenure (first 12 months).

Operational inefficiency: Resources wasted on onboarding customers who churn quickly.

Brand impact: Dissatisfied customers may influence reputation and reduce acquisition effectiveness.

## 🌟 Key Opportunities
Contract upgrades: Converting month-to-month customers into one- or two-year contracts.

Payment optimization: Promoting automatic bank transfer or credit card payments to reduce churn.

Service bundling: Offering packages with OnlineSecurity, TechSupport, and DeviceProtection to increase loyalty.

Targeted retention programs: Focusing on high-risk segments (seniors, low-tenure customers).

## ✅ Top Recommendations
Implement contract extension campaigns to lock in long-term customers.

Incentivize automatic payment adoption with discounts or loyalty rewards.

Design bundled service offers to enhance customer value and reduce churn.

Launch early-tenure retention programs to stabilize customers within the first year.

Continuously monitor churn KPIs with executive dashboards for proactive decision-making.

# 🔎 Detailed Churn Drivers & Retention Strategies

### 🟥1 Electronic Check (45.29%)

Cause: Perceived as inconvenient/insecure.

Strategy: Promote automatic payments with incentives.

### 🟥2 Month-to-Month Contract (42.71%)

Cause: Flexibility makes leaving easy.

Strategy: Upgrade campaigns to longer contracts.

### 🟥3 Fiber Internet (41.89%)

Cause: Service quality/support issues.

Strategy: Enhance reliability and proactive support.

### 🟥4 Senior Citizens (41.68%)

Cause: Difficulty with technology.

Strategy: Simplify packages and provide tailored support.

### 🟥5 Paperless Billing (33.59%)

Cause: Missed notifications or disconnection.

Strategy: Improve digital bill design and reminders.

### 🟥6 No Partner (32.98%)

Cause: Lack of shared motivation.

Strategy: Personalize offers and loyalty programs.

### 🟥7 No Dependents (31.28%)

Cause: Flexibility to switch providers.

Strategy: Competitive individual packages.

### 🟥8 Streaming TV (30.11%)

Cause: Quality issues or cheaper alternatives.

Strategy: Improve streaming quality and exclusive content.

### 🟥9 Streaming Movies (29.95%)

Cause: Competition from global platforms.

Strategy: Regional content and partnerships.

### 🟥10 Multiple Lines (28.65%)

Cause: Complex billing/high costs.

Strategy: Simplify billing and family discounts.

### 🟥11 Phone Service (26.75%)

Cause: Traditional service feels outdated.

Strategy: Integrate with modern bundles.

### 🟥12 No Phone Service (25.00%)

Cause: Service feels incomplete.

Strategy: Affordable add-on phone packages.

### 🟥13 Non-Senior (23.65%)

Cause: Younger customers churn due to competition.

Strategy: Youth-oriented offers and digital loyalty.

### 🟥14 Device Protection (22.54%)

Cause: Seen as unnecessary/costly.

Strategy: Tiered protection plans and bundling.

### 🟥15 Online Backup (21.57%)

Cause: Free alternatives undervalue service.

Strategy: Enhance usability, security, and bundle offers.

------------------------------------------------------------------------------------------

# 1️⃣2️⃣ Recommendations

## ⏱️ Short-term actions
Convert contracts: Target month-to-month customers with limited-time upgrades to 12–24 month terms.

Shift payments: Incentivize automatic bank transfer/credit card adoption to reduce churn risk.

Stabilize early tenure: Launch onboarding and retention offers focused on the first 12 months.

## 📈 Long-term actions
Bundle services: Offer value packs (security, support, protection) to increase stickiness and lifetime value.

Predictive retention: Deploy churn risk modeling to prioritize interventions and optimize spend.

Executive monitoring: Maintain real-time churn KPIs and segment dashboards for proactive decisions.

## ⚙️ Optimization suggestions
Segment-led offers: Tailor pricing and benefits by tenure, contract type, and payment method.

Service adoption growth: Promote add-ons that correlate with lower churn across key segments.

Outcome-based targets: Set quarterly churn reduction goals tied to revenue recovery.

## 🛡️ Risk mitigation
Reduce exposure: Limit reliance on manual payment methods via structured migration plans.

Protect vulnerable segments: Prioritize seniors and low-tenure customers with dedicated retention programs.

Govern performance: Establish clear accountability for churn KPIs and corrective actions.

## 🚀 Future Enhancements
Outline potential next steps such as predictive churn modeling, integration with CRM, or real-time dashboards.

## 📈 Planned Improvements
Detail specific improvements like automating data refresh, refining segmentation, or enhancing visualization.


-----------------------------------------------------------------------------------------------------

# 1️⃣3️⃣ Retention / Optimization Strategy

## 🔄 Customer Retention Strategy
Contract Upgrades: Encourage month-to-month customers to switch to one- or two-year contracts with loyalty incentives.

Payment Method Optimization: Promote automatic bank transfer and credit card payments to reduce churn risk.

Service Bundling: Offer packages that include OnlineSecurity, TechSupport, and DeviceProtection to increase customer stickiness.

Early-Tenure Programs: Focus retention efforts on customers within their first 12 months, where churn is highest.

Targeted Campaigns: Prioritize vulnerable segments such as senior citizens and low-service users with personalized offers.

--------------------------------------------------------------------------------------------------------------
# 1️⃣4️⃣ Additional Data Needed

## 📂 Missing Datasets
Customer satisfaction surveys to connect churn with service quality.

Marketing campaign data to measure impact of promotions on retention.

Competitor benchmarks for churn and retention rates to contextualize performance.

## 🌐 Useful External Data

Macroeconomic indicators (income levels, unemployment rates) to assess external churn drivers.

Industry averages for telecom churn to compare company performance.

Regional demographics to refine segmentation and tailor retention strategies.

## 🧾 Required Fields for Deeper Analysis

Customer acquisition cost (CAC) to calculate profitability per segment.

Lifetime value (CLV) to prioritize high-value customers.

Service usage frequency (calls, data, streaming) to identify behavioral churn patterns.

Complaint/issue logs to connect churn with unresolved service problems.

Languages spoken to tailor communication and support services.

Geographic location (city, region, rural vs. urban) to identify regional churn patterns.

Education level to analyze correlation with service adoption and churn.

Nationality to assess cultural or regulatory factors influencing churn.

Income brackets to link affordability with churn risk.

-------------------------------------------------------------

# 🗂 Files in This Repository

Telco-Customer-Churn-Analysis.pbix


# 🔗 Interactive Dashboard

You can explore the fully interactive dashboard online without needing Power BI Desktop. Click the link below to view the report:


https://app.powerbi.com/view?r=eyJrIjoiMWNlYzZlZWYtOTNmNC00NDhlLWFhYjUtMjkxNDFlZWY5MjNkIiwidCI6IjJiYjZlNWJjLWMxMDktNDdmYi05NDMzLWMxYzZmNGZhMzNmZiIsImMiOjl9


Note: The dashboard works best on desktop browsers. Mobile browsers may have limited functionality.


