# Telco Customer Churn Analysis (Power BI)

A two-page Power BI dashboard and slide deck that show which customers churn, why, and how much recurring revenue is at risk.

**Tools:** Power BI (Power Query, DAX), PowerPoint
**Dataset:** Telco Customer Churn (Kaggle), 7,043 customers

## Business problem

High churn in a competitive telecom market means lost recurring revenue, higher acquisition costs and lower customer lifetime value. This project answers:

- How many customers churn, and what does it cost?
- Which customer groups are highest risk?
- What drives churn, and what should the business do about it?

## Dashboard

**Page 1: Executive Overview and Revenue Impact**

![Executive overview](images/page1_executive_overview.png)

**Page 2: Risk Drivers and Cohort Analysis**

![Risk drivers](images/page2_risk_drivers.png)

## Key findings

| Metric | Result |
|---|---|
| Customers / churned | 7,043 / 1,869 |
| Overall churn rate | 26.54% |
| Monthly recurring revenue (MRR) churned | $139,130.85 (30.5% of total MRR) |
| Annualized revenue impact (projected) | about $1.67M |
| Month-to-month contract churn | 42.71% (two-year: 2.83%) |
| Fiber optic churn | 41.89% (DSL: 18.96%) |
| Electronic check churn | 45.29% |
| Churn in first 12 months | 47.44% (49-72 months: 9.51%) |
| Single customers, no dependents | 34.24% (partner + dependents: 14.24%) |
| Avg monthly bill, churned vs retained | $74.44 vs $61.27 |

**Revenue metric:** Annualized impact = MRR churned x 12, assuming lost customers are not replaced. It is a projection of recurring revenue at risk, not revenue already collected.

## Recommendations

1. Bundle tech support and online security into fiber optic plans.
2. Run a first-year onboarding program with check-ins at 30, 60 and 90 days.
3. Offer a small bill credit to move customers from electronic check to autopay.
4. Offer term-contract discounts to month-to-month customers early in their tenure.

## Method

- Cleaned blank values with Power Query.
- Built DAX measures for customers, churned customers, churn rate, MRR churned, revenue churn rate and annualized impact.
- Added calculated columns for tenure group, monthly charge band and family status, each with a sort-order column.
- Used a decomposition tree, clustered bar and column charts, and a Contract slicer.

## Repository contents

| File | Description |
|---|---|
| `Teleco Churn.pbix` | Power BI report (open with Power BI Desktop) |
| `Teleco-Customer-Churn.csv` | Raw dataset |
| `Teleco_Churn_Report_Presentation.pptx` | Slide deck |
| `images/` | Dashboard screenshots |

## How to open

Download `Teleco Churn.pbix` and open it in Power BI Desktop (free). If the data source path breaks, go to **Transform data > Data source settings** and point it to the CSV in this repo.
