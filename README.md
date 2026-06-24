Customer Behavior Analysis — Instacart RFM Segmentation
An RFM (Recency, Frequency, Monetary) analysis of ~206,000 Instacart customers using SQL window functions and Python visualization.

What It Does
Loads 5 Instacart CSV files (3M+ orders, 49K products) into a SQLite database
Computes RFM scores using NTILE(4) window functions
Segments customers into 5 groups: Best, Loyal, New, At Risk, Lost
Visualizes segment distribution and recency-frequency heatmap
Provides per-segment marketing recommendations
Files
File	Description
customerbehavior.ipynb	Full analysis notebook
instacart.db	SQLite database with relational schema
orders.csv, products.csv, aisles.csv, departments.csv, order_products__prior.csv, order_products__train.csv	Raw Instacart data
project_brief.docx	Project brief
What I Learned
Building a relational database in SQLite from CSV files
SQL window functions (NTILE, GROUP BY aggregations)
RFM customer segmentation methodology
Cross-tabulation and heatmap visualization
To Improve
Fix recency calculation (currently uses MIN(days_since_prior_order) instead of actual days since last order)
Verify segment percentages are computed, not hardcoded from the brief
