# Insurance-Claims-Fraud-Detection-Dashboard
 Power BI dashboard analyzing 10,000 insurance claims to detect fraud patterns across agents, vendors, and claim types | BFSI Domain
 # Insurance Claims Fraud Detection Dashboard

## 📊 Project Overview

A comprehensive Power BI dashboard analyzing **10,000 insurance claims** to detect fraud patterns across agents, vendors, claim types, and geographic regions. Built with BFSI domain focus, this project simulates real-world insurance fraud detection used by companies like EXL Service, Genpact, and HDFC.

---

## 🎯 Problem Statement

Insurance companies lose billions annually to fraudulent claims. Manual detection is slow, inconsistent, and error-prone. This dashboard provides a **data-driven fraud detection system** that helps insurance analysts:

- Identify high-risk agents and vendors
- Detect geographic fraud concentrations
- Analyze fraud patterns by claim type, severity, and customer demographics
- Enable drill-through investigation of individual agent transactions

---

## 🔍 Key Findings

| Finding | Detail |
|---|---|
| Overall Fraud Rate | 5.0% — 503 out of 10,000 claims are suspicious |
| Total Fraud Loss | $8.5M financial exposure |
| Highest State Fraud Rate | Kentucky — 6.4% |
| Highest Fraud Loss State | Vermont — $882K with only 579 claims |
| Highest Risk Agents | Ana Ashford & Lynette Curran — 50% fraud rate |
| Highest Risk Vendor | Thompson Inc — 6 fraud cases |
| Demographic Insight | Single claimants show higher fraud rate (5.4%) vs married (4.9%) |
| High Risk Agents | 18 agents show fraud rates above 30% |

---

## 📁 Dashboard Pages

### Page 1 — Welcome
- Project overview and navigation hub
- Dataset summary: 10,000 claims | 3 tables | Kaggle source

### Page 2 — Claims Overview
- 5 KPI cards: Total Claims, Claim Amount, Premium Amount, Avg Processing Days, YOY Growth
- Claims trend over time (field parameter — dynamic measure switching)
- Claims by Social Class, Marital Status, and State (map visual)
- Slicers: Year, Insurance Type

### Page 3 — Fraud Analysis
- 4 KPI cards: Total Fraud Claims, Fraud Rate %, Fraud Loss Amount, YTD Fraud Claims
- Fraud Rate trend Month-over-Month
- Fraud by Incident Severity, Age Group, Claim Size
- Claims Breakdown matrix by severity
- Slicers: Year, Incident Severity

### Page 4 — Agent & Vendor
- 4 KPI cards: High Risk Agent Count, Unemployed Fraud Rate, Avg Agent Experience, Total Agents
- Top 10 Agents by Fraud Rate
- Agent Risk vs Claim Amount (scatter plot)
- Top Vendors in Fraud Claims
- Top Agents by Fraud Loss table
- Slicers: Agent Type (Junior/Mid-Level/Senior), Year

### Page 5 — Agent Detail (Drill-Through)
- Drill-through from Page 4 agent visuals
- Agent-level KPIs: Total Claims, Fraud Claims, Fraud Rate %, Claim Amount, Fraud Loss
- Transaction Detail table
- Approved vs Declined donut chart
- Claims Breakdown by Severity

### Page 6 — Insights & Recommendations
- 9 data-backed key findings
- 7 actionable recommendations
- Management summary

---

## ⚙️ Technical Details

### Data Model
```
Star Schema — 5 Tables

FactClaims (10,000 rows — fact table)
    ├── DimAgent (1,200 agents)
    ├── DimVendor (600 vendors)
    ├── DimRiskScore (risk scoring)
    └── Date Table (custom date table)

Field Parameter Table — Select Measure (dynamic switching)
```

### DAX Measures (17 total)

**01 Basic Measures:**
- Total Claims, Total Fraud Claims, Fraud Rate %, Total Claim Amount, Total Premium Amount

**02 Intermediate Measures:**
- Avg Processing Days, Fraud Loss Amount, Large Claim Fraud Rate, Legitimate Claim Amount

**03 Time Intelligence:**
- MOM Fraud Rate, YTD Fraud Claims, YOY Claim Growth, MTD Premium

**04 Business Logic:**
- Agent Fraud Rate, Avg Agent Experience, High Risk Agent Count, Unemployed Fraud Rate

### Power Query — Engineered Columns (10+)

| Column | Logic |
|---|---|
| Fraud_Label | A → Approved, D → Declined-Suspicious |
| Age_Group | Young / Middle Aged / Senior |
| Claim_Size_Category | Small / Medium / Large |
| Processing_Days | Date difference calculation |
| Claim_Month | Month extracted from date |
| Claim_Quarter | Quarter extracted from date |
| Claim_Year | Year extracted from date |
| Agent_Type | Junior (0-4 yrs) / Mid-Level (5-9 yrs) / Senior (10+ yrs) |
| Risk_Level | Low / Medium / High based on risk score |
| Employment_Label | Employed / Unemployed label |

### Advanced Features
- **Drill-Through:** Page 4 → Page 5 agent-level investigation
- **Field Parameters:** Dynamic measure switching on trend charts
- **Tooltips:** Hover details on all major visuals
- **Cross-filtering:** All visuals interact with slicers
- **Conditional formatting:** Color-coded KPI cards and matrix tables

---

## 🛠️ Tools & Technologies

| Tool | Usage |
|---|---|
| Power BI Desktop | Dashboard development |
| Power Query (M) | Data cleaning and transformation |
| DAX | Measure creation and calculations |
| Star Schema | Data modeling |
| Kaggle | Dataset source |

---

## 📂 Dataset

**Source:** Kaggle — Insurance Claims Fraud Detection Dataset

| Table | Rows | Description |
|---|---|---|
| FactClaims | 10,000 | Main claims transaction table |
| DimAgent | 1,200 | Agent master data |
| DimVendor | 600 | Vendor master data |

**Usability Score:** 10/10
**Dataset Link:** [Kaggle — Insurance Claims Fraud Detection](https://www.kaggle.com/datasets/mastmustu/insurance-claims-fraud-data)

---

## 💡 Business Recommendations

1. Flag all claims above $50K for mandatory investigation
2. Audit the 18 high-risk agents immediately
3. Cross-verify Agent-Vendor pairs appearing in 3+ fraud cases
4. Implement automated severity-based claim review system
5. Prioritize Kentucky & Vermont for state-level fraud investigation
6. Immediately suspend Ana Ashford & Lynette Curran pending investigation
7. Audit Thompson Inc — pause new claim processing pending vendor review

---

## 🏗️ Project Structure

```
Insurance-Claims-Fraud-Detection-Dashboard/
│
├── Insurance_Fraud_Dashboard.pbix
│
├── screenshots/
│   ├── 01_Welcome.png
│   ├── 02_Claims_Overview.png
│   ├── 03_Fraud_Analysis.png
│   ├── 04_Agent_Vendor.png
│   ├── 05_Agent_Detail.png
│   └── 06_Insights.png
│
└── README.md
```

---

## 👤 About

**Preethiv Ram**
Data Analyst | BFSI Domain Focus

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://linkedin.com/in/preethivram)

---

## 📌 Other Projects

- [Credit Risk & Loan Performance Dashboard](https://github.com/preethivram-2k/credit-risk-loan-performance-dashboard) — Power BI | 89K+ loan records | BFSI domain

---

*Built with Power BI | June 2026*
 
