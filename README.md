# Sales Profitability Dashboard | Python, Excel, Power BI

## Objective
Find which customer segments, products and countries drive profit or loss
in a sales dataset of 700 orders (118.7M in total sales, Sep 2013 to Dec 2014).

## Tools
Python (Pandas), Excel (pivot tables and charts), Power BI Desktop

## Process
1. Data checking and preparation (Python/Pandas): confirmed no missing values
   or duplicate rows, removed an extra space from the "Sales" column name, kept
   "None" in Discount Band as a real value (no discount), and added a Discount % column.
2. EDA: grouped sales, profit and profit margin by segment, country, product and
   year, then examined the loss-making orders by discount band and product.
3. Dashboard (Power BI): built a dashboard with Sales and Profit KPI cards,
   sales vs profit by segment, product and country, and a sales trend.

## Key findings
- Total sales 118.7M, profit 16.9M (about 14% margin).
- Government (52.5M) and Small Business (42.4M) bring in most of the sales.
- Enterprise is the only segment that loses money (about -0.6M on 19.6M in sales).
  All 58 loss-making orders are Enterprise orders with High (33) or Medium (25)
  discounts. Enterprise orders with Low or no discount are profitable.
- Channel Partners have a very high margin (about 73%) but small sales (1.8M).
- 2013 covers only Sep to Dec, so year-to-year comparisons need care.

## Recommendation
Review pricing and discount rules for Enterprise orders with High and Medium
discounts, where all the losses occur (High: about -0.62M, Medium: about -0.15M).

## Next step
Enterprise has the lowest average discount (6.6%) of all segments, so compare
unit price against manufacturing price on these orders to check whether pricing,
not discount depth alone, drives the losses.

## Screenshots
![Dashboard](dashboard-page1.png)

## Files
- Dashboard_Report.pdf: Power BI dashboard export
- Capstone_Report.pdf: written analysis and insights
- Dashboard.pbix: Power BI file
- data_cleaning_eda.ipynb: Python (Pandas) analysis (run on Kaggle; change the file path to cleaned_sales.csv to run elsewhere)
- Capstone excel.xlsx: Excel pivot tables and charts
- cleaned_sales.csv: cleaned dataset
