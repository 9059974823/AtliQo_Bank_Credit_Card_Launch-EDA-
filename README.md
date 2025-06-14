# AtliQo_Bank_Credit_Card_Launch-EDA


AtliQo Bank Credit Card Launch – Exploratory Data Analysis
📑 Table of Contents
📌 Introduction

📊 Data Description
🧹 Data Cleaning
📈 Exploratory Data Analysis

Univariate Analysis
Bivariate Analysis
Multivariate Analysis

📉 Statistical Testing
🔍 Conclusion & Insights

📌 Introduction
AtliQo Bank is planning the launch of a new credit card and aims to better understand its existing customers to drive adoption. This exploratory data analysis (EDA) project helps uncover patterns in customer behavior, income, and spending habits to support product positioning and strategic marketing decisions.

![image](https://github.com/user-attachments/assets/889e9b7c-a5b2-4d59-a365-0f647d31cfa0)


📊 Data Description
The analysis is based on three integrated datasets provided by AtliQo Bank:

Customer Demographics Dataset

Contains personal and socio-economic information about customers.

Key columns:

Customer_ID
Age
Gender
Marital_Status
Occupation
Annual_Income
Location
Transaction Dataset

Captures historical credit card transactions.

Key columns:
Transaction_ID
Customer_ID
Transaction_Date
Transaction_Amount
Card_Type (Old or New card)
Merchant_Category

Credit Card Product Dataset

Describes features, benefits, and performance metrics of existing and new credit card offerings.

Key columns:
Card_Type
Features
Reward_Points
Annual_Fee
Eligibility_Criteria

These datasets were merged using Customer_ID and Card_Type where applicable.

🧹 Data Cleaning
A systematic approach was taken to prepare the data for analysis:

Missing Values

Numerical columns (like income) were filled using the median.

Categorical columns (like occupation or marital status) were filled using the mode or domain knowledge.

Outlier Treatment

Detected using boxplots and domain rules.

For example, customers with annual income below $100 were treated as outliers and replaced with occupation-wise median income.

Data Type Consistency

Ensured all columns had consistent formats, e.g., Transaction_Date was converted to datetime.

Duplicate Removal

Removed any repeated Transaction_ID or Customer_ID entries after validating uniqueness.

Feature Engineering (optional)

Derived fields like:

Transaction_Month
Customer_Age_Group
Income_Bracket

📈 Exploratory Data Analysis
🔹 Univariate Analysis
Age: Histogram revealed the bank has a large share of young customers (18–30 age group).

Annual Income: Right-skewed distribution with a few high-income earners.

Occupation: Majority are salaried professionals and business owners.

🔸 Bivariate Analysis
Income vs. Occupation:

Business owners earn significantly more on average than other groups.

Income vs. Gender:

Slight income gap observed, with males having a slightly higher median income.

Transaction Amount vs. Age:

Middle-aged customers tend to make higher-value transactions.

🔺 Multivariate Analysis
Analyzed the interaction between gender, occupation, and income, revealing that:

Female business owners still earn less on average than male counterparts.

Salaried customers are evenly distributed across income brackets.

📉 Statistical Testing
🧪 Hypothesis Testing – Two Sample Z-Test
Goal: Determine if the new credit card has significantly impacted transaction behavior.

Null Hypothesis (H₀):
No difference in transaction amount between customers using old vs. new credit card.

Alternative Hypothesis (H₁):
Customers using the new credit card have significantly higher transaction amounts.

Test Result:

Z-score exceeded critical value

p-value < 0.05
→ Rejected H₀: New card shows statistically significant improvement.

🔍 Conclusion & Insights
High-Income Segments: Business owners and senior professionals show higher transaction values.

Young Customers: Aged 18–25, forming 26% of the base, are underutilizing credit cards—representing an opportunity for low-limit, no-fee offerings.

Product Validation: Statistical tests confirm that the new credit card offering improves customer engagement and spending
