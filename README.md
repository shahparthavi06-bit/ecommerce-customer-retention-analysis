# E-commerce Customer Retention & RFM Segmentation Analysis

## Business Problem

A UK-based online retailer wanted to understand which customers drive revenue, why customers churn, and where retention efforts should be focused. This project analyses 13 months of transaction data to answer those questions using RFM segmentation and cohort retention analysis.

## Dataset

- **Source**: UCI Online Retail Dataset
- **Size**: 541,909 transactions across 4,372 customers and 38 countries
- **Period**: December 2010 – December 2011
- **Cleaning**: Removed 144,025 rows (missing CustomerIDs, cancellations, invalid quantities/prices), retaining 397,884 valid transactions from 4,338 customers

## Methodology

1. **Data Cleaning** — handled missing values, removed cancelled orders, calculated revenue per line item
2. **Exploratory Analysis** — monthly revenue trends, geographic revenue distribution, average order value
3. **RFM Segmentation** — scored customers on Recency, Frequency, and Monetary value using quintile-based scoring; classified into Champions, Loyal, At Risk, and Lost segments
4. **Cohort Retention Analysis** — tracked monthly retention rates for each acquisition cohort to identify churn patterns over time

## Key Findings

1. **Revenue is highly concentrated**: Champions (21.5% of customers) generate 70.2% of total revenue (£6.26M), while At Risk and Lost customers (55.3% combined) contribute just 14%.

2. **Month-1 retention is the biggest drop-off point**: Average retention falls to ~22% by the second month across most cohorts, indicating that the post-first-purchase period is the highest-leverage point for intervention.

3. **Early cohorts show stronger long-term loyalty**: The December 2010 cohort retained 35-40% of customers in later months, notably higher than subsequent cohorts — worth investigating what drove this (e.g. promotional terms, product mix).

4. **Revenue is geographically concentrated**: The UK accounts for 82% of total revenue, with minimal diversification across the other 37 countries.

## Recommendations

- **Onboarding campaign**: Launch a targeted email sequence for first-time buyers to improve Month-1 retention
- **Loyalty programme**: Build a rewards tier for the 934 "Champions" customers who drive the majority of revenue
- **Win-back campaign**: Target the 1,092 "At Risk" customers with re-engagement offers before they churn entirely
- **Geographic expansion**: Explore growth opportunities in underrepresented markets (Netherlands, Germany, France currently <2% each)

## Tools Used

- **Python**: pandas, numpy for data cleaning and RFM scoring
- **Matplotlib & Seaborn**: visualisations and cohort heatmap
- **Jupyter Notebook**: end-to-end analysis

## Files

- `notebooks/analysis.ipynb` — full analysis notebook
- `data/eda_charts.png` — revenue trend and country breakdown
- `data/cohort_heatmap.png` — customer retention heatmap
