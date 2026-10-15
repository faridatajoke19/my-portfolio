# Project 3 — SQL Data Analysis

Tagline: Use T-SQL to answer business questions — counts, revenue breakdowns, monthly trends, and filtered analytics.

Summary
This project performs SQL-based analysis of the cleaned orders dataset using Microsoft SQL Server / SSMS. The queries explore filters, aggregations, ordering, and combined queries to derive business metrics such as top products, revenue by referral source, and monthly volumes.

Role & timeline
- Role: Data Analytics Intern — Aliu Faridat Ajoke  
- Timeline: Internship project (add exact dates or duration)

Tools & tech
- Microsoft SQL Server Management Studio (SSMS)  
- T-SQL (SELECT, WHERE, GROUP BY, HAVING, ORDER BY, aggregates)

Key work & approach
- Created the DecodeLabsOrders database and an orders table to match the dataset schema.
- Imported the CSV into the orders table and executed a suite of queries to extract insights.
- Wrote queries for filtering (e.g., cancelled orders), aggregations (SUM, AVG, COUNT), and monthly grouping.

Representative queries (examples)
- View top 10 highest-value orders:
```sql
SELECT TOP 10 OrderID, Product, TotalPrice
FROM orders
ORDER BY TotalPrice DESC;
```
- Monthly order volume:
```sql
SELECT FORMAT(Date, 'yyyy-MM') AS OrderMonth, COUNT(*) AS OrdersThatMonth
FROM orders
GROUP BY FORMAT(Date, 'yyyy-MM')
ORDER BY OrderMonth ASC;
```
- Revenue per Referral Source:
```sql
SELECT ReferralSource, SUM(TotalPrice) AS TotalRevenue, COUNT(*) AS OrderCount
FROM orders
GROUP BY ReferralSource
ORDER BY TotalRevenue DESC;
```

Full query set
- See the complete query file: project3_queries.sql — https://github.com/faridatajoke19/DecodeLabs-internship/blob/main/project3_queries.sql

Key findings (from queries)
- Total orders: 1,200
- Printer, Tablet, and Chair are among the top-selling products
- Online and Cash are top revenue-generating payment methods after excluding cancelled orders
- Monthly orders are steady without an obvious seasonal pattern

Artifacts & links
- SQL queries: project3_queries.sql — https://github.com/faridatajoke19/DecodeLabs-internship/blob/main/project3_queries.sql
- Project notes: README_Project3.md — https://github.com/faridatajoke19/DecodeLabs-internship/blob/main/README_Project3.md
