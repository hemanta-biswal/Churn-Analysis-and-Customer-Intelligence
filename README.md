# 📊 Churn Analysis & Customer Intelligence

### End-to-End Customer Churn Analytics using SQL & Python

> **Business-focused data analytics project to identify churn drivers, quantify revenue impact, and develop actionable customer retention strategies.**

---

## 📌 Executive Summary

Customer retention is a critical business challenge for subscription-based businesses. In a highly competitive OTT market, understanding **who is leaving, why they are leaving, and when they are most likely to leave** is essential for protecting recurring revenue and customer lifetime value.

This project develops an end-to-end **Customer Churn Analytics pipeline** using a relational customer database and Python-based analytical workflows.

The analysis integrates customer demographics, subscription characteristics, contract structures, plan tiers, financial metrics, and customer support interactions to identify high-risk customer segments and quantify their business impact.

### Key outcomes

- Analyzed **20+ business KPIs**
- Identified significant churn differences between **monthly and annual contracts**
- Quantified **revenue loss and CLTV impact**
- Analyzed churn across plans, states, customer segments, and support behavior
- Identified high-risk customer cohorts for retention campaigns
- Translated analytical findings into **data-driven business recommendations**

---

# 🎯 Business Problem

The business wants to reduce customer churn while protecting recurring revenue.

The analysis focuses on three fundamental questions:

### 01 — WHO?

Which customers are most likely to churn?

### 02 — WHY?

What customer behaviors, subscription characteristics, and support interactions are associated with churn?

### 03 — WHEN?

When does churn become most likely during the customer lifecycle?

The ultimate objective is to convert raw customer data into **actionable retention strategies**.

---

# 🏢 Business Context

Although the project is demonstrated using an OTT/subscription business model, the analytical framework is applicable to multiple industries.

| Industry | Churn Definition |
|---|---|
| **OTT / Streaming** | Subscription cancellation |
| **SaaS** | Subscription or account cancellation |
| **E-commerce** | No purchase for a defined period |
| **Telecom** | Account termination |
| **Banking** | No transactions for a defined period |
| **AdTech** | Significant reduction in platform engagement |
| **Membership** | Membership inactivity |

---

# 🛠️ Technology Stack

### Data & Programming
- **Python**
- **Pandas**
- **NumPy**

### Database & Querying
- **SQL**
- **SQLite**
- `sqlite3`

### Visualization
- **Matplotlib**
- **Seaborn**

### Analytical Techniques
- Data Cleaning
- Data Quality Validation
- Feature Engineering
- Exploratory Data Analysis
- Customer Segmentation
- KPI Development
- Cohort Analysis
- Behavioral Analysis
- Revenue Impact Analysis
- Churn Risk Analysis
- Business Insight Generation

---

# 🏗️ Analytical Architecture

```text
                 ┌─────────────────────┐
                 │   Customer Data     │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │   SQLite Database   │
                 │                     │
                 │  Customer           │
                 │  Subscription       │
                 │  Support            │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │   SQL Extraction    │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Python + Pandas     │
                 │ NumPy               │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Data Cleaning &     │
                 │ Quality Checks      │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Feature Engineering │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Exploratory &       │
                 │ Churn Analysis      │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Visualization &     │
                 │ KPI Reporting       │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Business Insights & │
                 │ Retention Strategy  │
                 └─────────────────────┘
```

---

# 🗄️ Data Model

**Database:** `customer_churn`

The project uses a relational structure consisting of three primary tables.

### `db_customer`

Contains customer demographic and profile information.

```text
customerid
name
country
state
gender
dob
interests
pincode
```

### `db_subscription`

Contains subscription, contract, financial, and churn information.

```text
customerid
subscription_start_date
subscription_type
renewal_date
plan_type
contract_type
cancellation_date
cancellation_reason
monthly_charges
cltv
churn_score
```

### `db_support`

Contains customer support and service interaction information.

```text
customerid
complaint_date
escalations
csat_score
comment
```

---

# 🔄 Project Workflow

## 1. Data Extraction

Connected Python to the SQLite relational database and extracted relevant datasets using SQL.

### Activities

- Database connection
- SQL querying
- Multi-table joins
- Column selection
- Data import into Pandas

---

## 2. Data Cleaning

Prepared the raw data for reliable analysis.

### Activities

- Data type validation
- Missing-value handling
- Duplicate detection
- Column standardization
- Date validation
- Categorical-value validation
- Data quality checks

---

## 3. Feature Engineering

Created analytical variables required for churn and customer-value analysis.

### Key Features

- Customer age
- Customer tenure
- Churn flag
- Churn risk category
- Revenue at risk
- Revenue loss
- CLTV impact
- Complaint indicators
- Escalation indicators

---

## 4. Exploratory Data Analysis

Performed multi-dimensional analysis to identify churn patterns.

### Analysis Dimensions

- Plan type
- Contract type
- Subscription type
- Geography
- Customer age
- Tenure
- Monthly charges
- CLTV
- Support escalations
- Complaints
- Churn score
- Cancellation period

---

# 📐 Business KPIs

| KPI | Calculation |
|---|---|
| **Churn Rate** | Churned Customers / Total Customers |
| **Retention Rate** | 1 − Churn Rate |
| **ARPU** | Revenue / Active Customers |
| **Average Tenure** | Average Customer Tenure |
| **Revenue at Risk** | Revenue from High-Risk Customers |
| **Revenue Loss** | Revenue associated with churned customers |
| **CLTV Lost** | CLTV associated with churned customers |
| **Escalation Rate** | Escalations / Complaints × 100 |
| **Avg. Complaints / Customer** | Total Complaints / Unique Customers |
| **Plan Churn Rate** | Churn Rate by Plan |
| **Geographic Churn** | Churn Rate by Country / State |
| **Contract Churn** | Churn Rate by Contract Type |

---

# 📊 Key Findings

## Overall Customer Retention

| Metric | Result |
|---|---:|
| **Churn Rate** | **28.6%** |
| **Retention Rate** | **71.4%** |
| **Average Tenure** | **1,451 days** |
| **ARPU** | **₹18.8** |
| **Revenue Loss** | **₹74** |
| **Revenue Loss %** | **18%** |
| **CLTV Lost** | **₹2,047** |

---

## Contract-Level Churn

One of the strongest patterns identified was the substantial difference between monthly and annual subscribers.

| Contract Type | Churn Rate |
|---|---:|
| **Monthly** | **55.6%** |
| **Annual** | **8.3%** |

### Business Interpretation

Monthly subscribers represent a significantly higher churn-risk segment.

This creates an opportunity to develop targeted **monthly-to-annual contract migration campaigns**, particularly for customers with high CLTV and high churn scores.

---

## Plan-Level Churn

The **Basic plan** accounts for the largest share of churned customers.

However, customer volume should not be considered in isolation.

The business should evaluate:

```text
Churn Volume
+
Revenue Contribution
+
CLTV
+
Churn Risk
```

to identify the customers who create the greatest financial exposure.

---

## Geographic Churn

**Karnataka** recorded the highest observed churn concentration.

This requires further root-cause analysis around:

- Pricing changes
- Product/service issues
- Customer complaints
- Technical problems
- Customer support
- Competitor activity

---

## Temporal Churn Pattern

The analysis identified **September 2024** as a period with particularly high churn.

This should be investigated alongside potential changes in:

- Subscription pricing
- Product experience
- Customer support
- Contract policies
- Competitor offers
- Marketing campaigns

---

# 💰 Revenue Impact

Churn represents more than lost customers.

It directly affects:

### Recurring Revenue

Customers who cancel their subscriptions reduce future recurring revenue.

### Customer Lifetime Value

High-value customers leaving the platform can create substantial long-term financial impact.

### Acquisition Efficiency

When churn is high, the company must continuously acquire new customers simply to replace lost subscribers.

Therefore:

> **Retention is not only a customer-experience problem; it is a revenue-protection problem.**

---

# 🎯 Customer Retention Strategy

Based on the analysis, the following actions are recommended.

## 1. Monthly → Annual Migration

Identify high-risk monthly subscribers and provide targeted annual-plan incentives.

Possible approaches:

- Personalized discounts
- Annual-plan benefits
- Loyalty rewards
- Longer-term pricing incentives

---

## 2. High-Value Customer Prioritization

Prioritize customers using a combination of:

```text
Churn Score
+
CLTV
+
Monthly Charges
+
Customer Tenure
+
Support Escalations
```

### Priority Segment

**High churn risk + High CLTV + High revenue contribution**

These customers should receive proactive retention intervention.

---

## 3. Investigate Karnataka

Conduct a deeper regional analysis to determine whether churn is associated with:

- Price changes
- Service quality
- Technical issues
- Customer complaints
- Support performance
- Competitor activity

---

## 4. Investigate September 2024

Perform a before-vs-after analysis around September 2024 to identify potential business or operational changes that could have influenced churn.

---

## 5. Proactive Customer Outreach

High-risk customers can be targeted through:

- Email
- SMS
- Phone calls
- Personalized offers
- Customer support interventions

---

# 📈 Recommended Analytical Dashboard

A production-ready dashboard could monitor:

### Executive KPIs

- Total Customers
- Active Customers
- Churned Customers
- Churn Rate
- Retention Rate
- Revenue at Risk
- CLTV Lost

### Customer Analysis

- Churn by Plan
- Churn by Contract
- Churn by State
- Churn by Age Group
- Churn by Tenure
- Churn by Subscription Type

### Behavioral Analysis

- Churn vs Complaints
- Churn vs Escalations
- Churn vs CSAT
- Churn vs Monthly Charges
- Churn vs CLTV

### Trend Analysis

- Monthly Churn
- Revenue Loss Trend
- Customer Acquisition vs Churn
- Contract Migration

---

---

# 🧠 Skills Demonstrated

### Technical

`SQL` `Python` `Pandas` `NumPy` `SQLite` `Matplotlib` `Seaborn`

### Analytics

`Data Cleaning` `EDA` `Feature Engineering` `KPI Analysis` `Customer Segmentation` `Churn Analysis` `Revenue Analysis`

### Business

`Retention Strategy` `Revenue Impact Analysis` `Customer Intelligence` `Actionable Insights` `Executive Reporting`

---

# 📚 Key Learnings

This project strengthened my ability to work through a complete analytics lifecycle:

```text
Business Problem
       ↓
Data Extraction
       ↓
Data Cleaning
       ↓
Feature Engineering
       ↓
Exploratory Analysis
       ↓
KPI Development
       ↓
Visualization
       ↓
Business Insights
       ↓
Strategic Recommendations
```

The key takeaway was learning to move beyond simply **"analyzing data"** and instead use data to answer:

> **What happened? → Why did it happen? → Who is affected? → What should the business do next?**

---



# 💼 Business Impact

The project demonstrates how customer-level data can be transformed into actionable retention intelligence.

The analysis identified:

- A **28.6% overall churn rate**
- A significant **monthly vs annual contract churn gap**
- **18% revenue loss** associated with churn
- **₹2,047 in CLTV loss**
- High churn concentration in **Karnataka**
- A significant churn period around **September 2024**
- High-value customers requiring proactive retention attention

These findings provide a foundation for developing a **data-driven customer retention strategy** focused on protecting recurring revenue and customer lifetime value.

---

# 👨‍💻 Author

## Hemanta Biswal

**Data Analyst | Data Engineer | Data & AI Enthusiast**

I enjoy transforming raw data into actionable insights using **SQL, Python, Power BI, and modern data engineering technologies**.

### Areas of Interest

`Data Analytics` • `Data Engineering` • `Business Intelligence` • `Machine Learning` • `Cloud Data Platforms`

---

## ⭐ Project

If you find this project useful, consider giving the repository a ⭐.

**Built with:**  
`Python` · `SQL` · `Pandas` · `NumPy` · `SQLite` · `Matplotlib` · `Seaborn`
