# Project 2 — Exploratory Data Analysis (EDA)

Tagline: Descriptive statistics, pivot tables, monthly trends, and outlier detection on the cleaned orders dataset.

Summary
This project performs EDA on the cleaned orders dataset (1,200 records) to surface patterns in sales, customer behavior, and order fulfillment. The analysis revealed top products, payment-method revenue, and outlier orders.

Role & timeline
- Role: Data Analytics Intern — Aliu Faridat Ajoke  
- Timeline: Internship project (add exact dates or duration)

Tools & tech
- Microsoft Excel (PivotTables, formulas, charts)

Key findings (high level)
- Total orders: 1,200
- Average order value: $1,053.97 (median: $823.62) — right-skewed distribution
- Top products by order count: Printer, Chair, Tablet
- Cancelled + Returned orders make up ~41.4% of total orders
- Monthly order volume: steady (27–53 orders/month)
- Outliers: 8 orders above the upper IQR bound (all verified as legitimate)

Approach
- Calculated descriptive statistics (mean, median, mode, min, max, sum) for numeric fields.
- Built PivotTables for breakdowns by Product, Order Status, Payment Method, and Referral Source.
- Created a monthly trend chart from Jan 2023 to Jun 2025.
- Conducted outlier detection using the IQR method.

Technical notes
- All calculations built using Excel functions: AVERAGE, MEDIAN, QUARTILE, SUM, COUNT, and PivotTable aggregations.
- Outliers identified with Q1, Q3, IQR = Q3 - Q1, and any point > Q3 + 1.5 * IQR flagged.

Business impact
- Verified data quality and business patterns used by Project 3 (SQL analysis) and Project 4 (dashboard).
- Identified high-value orders and returned/cancelled order proportion, which are actionable for operations and customer-retention conversations.

Artifacts & links
- EDA workbook: Project 2 (Dataset for Data Analytics).xlsx — https://github.com/faridatajoke19/DecodeLabs-internship/blob/main/Project%202%20(Dataset%20for%20Data%20Analytics).xlsx
- Project notes: README (Project 2) — https://github.com/faridatajoke19/DecodeLabs-internship/blob/main/README.md
