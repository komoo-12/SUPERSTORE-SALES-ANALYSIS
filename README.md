# SUPERSTORE-SALES-ANALYSIS
## PROJECT OVERVIEW
Dataset	Superstore Sales (Kaggle)
Records	9,994 order lines, 21 columns
Period	January 2014 to December 2017
Tool	Microsoft Excel (formulas, Excel Tables, charts, data validation)
Goal:	Import, clean, and organize sales data; summarize revenue, units sold, and monthly trends; visualize overall performance
### WORKBOOK CONTENTS
Sheet	Purpose
Dashboard	KPI cards, 5 charts, Slicers, key takeaways
Summary	Formula-driven summary tables (pivot equivalents) that feed the dashboard
Data	Cleaned dataset as an Excel Table (tblSales) with helper columns
Notes	Cleaning log, formula documentation, assumptions, steps to build native PivotTables
Process
1. Import and clean
Loaded the CSV and checked quality: no blank cells, no duplicate rows, unique Row ID.
Converted text dates (m/d/yyyy) to real Excel dates.
Sorted rows by order date and order ID so each order's lines are contiguous.
Applied header styling, number formats.
2. Add helper columns (formulas)
Column	Formula idea	Use
Year / Month No	YEAR(), MONTH()	Time grouping
Month Start	DATE(year, month, 1)	
Discount Band	Nested IF into 0%, 1-10%, 11-20%, 21-30%, 31-50%, Over 50%	Discount analysis
Profit Margin	Profit / Sales	Profitability
3. Summarize with pivot-style tables
SUMIFS formulas on the Summary sheet reproduce PivotTable results for KPIs, yearly performance, category, region, segment, sub-category, discount band, and selected states. The year dropdown on the Dashboard filters these tables.
To build native PivotTables instead: Insert > PivotTable on the Data table, put Month Start (grouped by Months and Years) in Rows and Sales, Profit, Quantity in Values, then repeat with Category, Region, and Sub-Category. Add Slicers for Year, Region, and Category.
4. Build the dashboard
   4 KPI cards (sales, profit, margin, units sold) and 5 charts:  category, region, yearly performance, profit by discount level, and profit by sub-category.
Key Metrics
Metric	Value
Total sales (revenue)	$2,297,201
Total profit	$286,397
Profit margin	12.03%
Units sold	37,873

### Business Questions and Findings

1. What is overall performance? $2.30M in sales and $286K profit (12.5% margin) and 37,873 units.

2. How is the business trending year over year? Sales dipped 3% in 2015, then grew 29% in 2016 and 20% in 2017 to $733K. Margin held at about 12-13% from 2015 onward. Growth comes mainly from more orders (969 in 2014 to 1,687 in 2017).

3. When do we sell the most? September, November, and December are the peak months; January and February are the weakest. Inventory and staffing should be planned around Q4.

4. Which categories make money? Technology ($836K sales, 17% margin) and Office Supplies ($719K, 17%) drive profit. Furniture has $742K in sales but only $18K profit (2% margin).

5. Which products lose money? Tables (-$17.7K), Bookcases (-$3.5K), and Supplies (-$1.2K) lose money overall. Machines have $189K in sales but only $3K profit. Copiers, Paper, Accessories, and Envelopes earn the highest margins.

6. Is discounting hurting profit? Lines with no discount earn about a 30% margin. Anything above 20% discount loses money, and lines above 50% lose about $1.19 for every $1 of sales. About 19% of all order lines are unprofitable, totalling about -$156K. Tables and Bookcases are discounted heavily (21-26% on average).

7. Which regions perform best and worst? West leads (15% margin on $725K), East is 13%, South is 12%, and Central is weakest at 8%, where Furniture is loss-making.

8. Which states are problem areas? Texas (-$25.7K), Ohio (-$17.0K), and Pennsylvania (-$15.6K) lose the most. California ($76K) and New York ($74K) earn the most profit.

9. Which customer segments matter most? Consumer is about half of sales ($1.16M, 12% margin); Corporate (13%) and Home Office (14%) are slightly more profitable per dollar. The top 20% of customers account for about 48% of sales.

Recommendations
Cap discounts at about 20% and review pricing on Tables, Bookcases, and Machines first.
Investigate the Central region and the Texas, Ohio, and Pennsylvania cluster, where discounting and Furniture mix are likely drivers.
Promote high-margin lines such as Copiers, Paper, and Accessories.
Build inventory and staffing ahead of the September-December peak.
### source of the data
Download Superstore_Sales_Dashboard.xlsx and open it in Excel.
Go to the Dashboard sheet and choose a year in cell C3 to filter the KPIs and charts. The monthly trend and yearly charts always show all years.
### Limitations
Revenue is the Sales column, which is already net of discount in this dataset.
Summary tables use SUMIFS formulas rather than native PivotTables so the dashboard recalculates and the year filter works.
The sub-category chart is ordered by all-time profit and does not re-sort when the year filter changes.
The key takeaways text on the Dashboard is based on all years and does not change with the filter.
Findings are descriptive. Discounting is associated with losses here, but this analysis does not prove causation.
### Skills Demonstrated

Data cleaning, Excel formulas (SUMIFS, IF, DATE, YEAR, MONTH), Excel Tables, data validation, dashboard design, data visualization, and business insight writing.

Dataset Source

Superstore Sales Dataset, Kaggle.
