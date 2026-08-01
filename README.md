# 🏦 Banking Analytics Dashboard

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-005C9C?style=for-the-badge&logo=microsoft&logoColor=white)
![Power Query](https://img.shields.io/badge/Power_Query-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Business Intelligence](https://img.shields.io/badge/Business_Intelligence-107C10?style=for-the-badge&logo=microsoft&logoColor=white)

## 📌 Project Overview
This project is an end-to-end **Financial Analytics** solution designed to monitor, analyze, and optimize banking operations. By transforming raw banking data into an interactive **Power BI Dashboard**, this project provides executives and branch managers with actionable insights into customer behavior, account stability, transaction volumes, and support center efficiency.

### 🎯 Business Problem
The bank lacked a centralized reporting system. Executive teams were struggling to connect customer profiles with their respective financial products (loans, cards, checking/savings accounts) and support tickets. This siloed data prevented leadership from identifying cross-selling opportunities and addressing customer service bottlenecks.

### 💡 Objectives
- Develop a comprehensive **Executive Dashboard** to track overarching financial KPIs.
- Analyze customer demographics and account dormancy to improve retention.
- Evaluate loan and credit card distributions to assess risk and profitability.
- Measure support center performance to enhance customer satisfaction.

## 🚀 Features

### 📊 Financial KPIs Tracked
* **Total Balance:** $254.66M
* **Total Customers:** 5,050
* **Total Loan Amount:** $644.33M
* **Active Accounts:** 5,062 (99.25% Active Rate)
* **Support Resolution Rate:** 49.32%
* **Active Cards:** 3,809

### 📑 Dashboard Pages
1. **Executive Overview:** High-level summary of total balances, deposits, and loan amounts filtered by state and account type.
2. **Customer Analytics:** Demographic breakdowns, customer growth metrics, and product adoption rates.
3. **Account Analytics:** Detailed view of active vs. dormant accounts and top 10 customers by balance.
4. **Transaction Analytics:** Seasonal and monthly trends across deposits, payments, transfers, and withdrawals.
5. **Loan Analytics:** Risk assessment tracking $644.33M in loans across Business, Education, Home, Personal, and Car categories.
6. **Card Analytics:** Monitoring 4,000 total cards, including 83 expiring within 30 days, distributed across Credit, Debit, and Prepaid.
7. **Support Center:** Performance metrics analyzing 3,100 calls, issue types, and resolution rates.

---

## 🔍 Insights & Business Value
- **Customer Service Bottleneck:** The support center is struggling with a 49.32% resolution rate out of 3,100 calls, identifying a critical area for operational improvement.
- **Strong Account Retention:** With 99.25% of accounts remaining active and only 38 dormant accounts, the bank has excellent baseline retention.
- **Balanced Transaction Volume:** Transaction types are evenly distributed (Deposits, Payments, Transfers, and Withdrawals all hover around 24.6% - 25.2%), indicating healthy, multi-use customer behavior.
- **Loan Distribution:** Loans are robustly distributed, with Personal ($161M), Home ($160M), and Education ($154M) driving substantial revenue.

---

## 🛠️ Technical Implementation

### Data Model
- Implemented a robust **Star Schema** with centralized fact tables (Transactions, Support Calls, Loans) surrounded by dimension tables (Customers, Dates, Account Types).
- Established one-to-many relationships for optimized DAX query performance.

### Data Cleaning & Power Query
- Standardized data formats across multiple source files.
- Handled missing values in customer demographic fields.
- Created conditional columns for mapping seasonal trends (Spring, Summer, Fall, Winter) to specific transaction dates[cite: 1].
- Built custom date tables for time-intelligence calculations.

### DAX Measures
- `Customer Growth %` = Year-over-year calculation of new customer acquisition.
- `Resolution Rate` = `DIVIDE([Resolved Calls], [Total Calls], 0)`.
- `Expiring in 30 Days` = Filtered count of cards with expiration dates falling within the next month.

### Visualizations & UX/UI
- **Color Theme:** Professional teal, blue, and navy palette ensuring high contrast and modern aesthetics.
- **Navigation:** Persistent sidebar navigation enabling seamless transitions between the 7 reporting pages.
- **Slicers:** Intuitive filtering by Account Type, State, Customer Segment, Date, and Issue Type.

---

## 🌐 Live Dashboard

View the interactive dashboard here:

[Open Power BI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiNDBmNGQ4YmYtYzAxMi00ZDdmLTkwY2MtZTk2ZDA2NjAxZDQwIiwidCI6IjJiYjZlNWJjLWMxMDktNDdmYi05NDMzLWMxYzZmNGZhMzNmZiIsImMiOjl9&pageName=92b2ec39c9dc2e010d22)

---

## 📚 Lessons Learned
- Advanced my understanding of **DAX Time-Intelligence** functions to accurately report on customer tenure and historical loan amounts.
- Improved UX/UI design principles by organizing a massive amount of banking KPIs into easily digestible, single-page views without clutter.
- Learned the importance of data granularity when connecting transaction-level data with overarching customer dimension attributes.

## 🚀 Future Improvements
- Integrate a machine learning model to predict customer churn based on transaction frequency and account dormancy.
- Add Row-Level Security (RLS) so branch managers can only view data specific to their region or state.
- Implement a drill-through feature to view individual transaction histories directly from the top 10 customer list.

## ✍️ Author
*(Mohamed Samir)*
Data Analyst | Power BI Developer
