# Project 1 — Data Cleaning

Tagline: Cleaned and prepared a 1,200-row e-commerce orders dataset for reliable analysis and visualization.

Summary
This project produced a canonical, cleaned dataset used across the internship projects. Cleaning steps removed missing values, fixed date formats, resolved duplicates, and standardized categorical fields so later analysis and visualization could rely on consistent data.

Role & timeline
- Role: Data Analytics Intern — Aliu Faridat Ajoke  
- Timeline: Internship project (add exact dates or duration)

Tools & tech
- Microsoft Excel (cleaning, formulas, filters)

Problem statement
The raw e-commerce orders dataset contained inconsistent date formats, possible duplicates, mixed-case and misspelled categorical values, and numeric fields stored as text — which would cause errors and misleading results for downstream EDA and visualizations.

Goals & success metrics
- Produce a single cleaned dataset with consistent types and no duplicates.
- Ensure 100% non-null values for required columns.
- Produce a stable source for Projects 2–4.

Approach
- Inspected columns for nulls and inconsistent formats.
- Standardized date formats and converted date-like columns to proper Date types.
- Normalized categorical fields (Product, PaymentMethod, OrderStatus, ReferralSource, CouponCode) by correcting casing and typos.
- Converted numeric fields (Quantity, UnitPrice, TotalPrice, ItemsInCart) to numeric types and validated ranges.
- Removed duplicate rows and verified unique OrderIDs.

Technical implementation
- All cleaning performed in Excel:
  - Used text functions (TRIM, UPPER/LOWER, SUBSTITUTE) to normalize strings.
  - Used DATEVALUE and cell reformatting for consistent dates.
  - Sorted by OrderID and used Excel’s Remove Duplicates feature; validated uniqueness via `COUNTIF`.
  - Used value conversions and reformatting for numeric fields.

Challenges & tradeoffs
- Hand-cleaning in Excel scales to this dataset (1,200 rows) but would not be ideal for larger production datasets.
- For reproducibility, saving the cleaned output and documenting steps was necessary — automation (scripts) is a next step.

Results & impact
- Final cleaned dataset: 1,200 rows × 14 columns
- No missing values or duplicate OrderIDs
- All categorical fields standardized into small controlled vocabularies (Product: 7 values; PaymentMethod: 5 values; etc.)
- Ready-to-use dataset for analysis and dashboarding

Learnings & next steps
- For repeatable pipelines, migrate these cleaning steps to a script (Python/pandas or T-SQL ETL).
- Add validation checks and unit tests for dataset health on new imports.

Artifacts & links
- Cleaned dataset: Project1_Cleaned_Dataset.xlsx — https://github.com/faridatajoke19/DecodeLabs-internship/blob/main/Project1_Cleaned_Dataset.xlsx
- Project notes: README_Project1.md — https://github.com/faridatajoke19/DecodeLabs-internship/blob/main/README_Project1.md
