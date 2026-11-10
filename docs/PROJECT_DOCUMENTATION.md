# Project Documentation

## 1. Project summary

The Retail Business Performance Dashboard is an Excel-based business intelligence solution that summarizes retail performance for January 2024 through December 2025. It combines sales, returns, and target information with descriptive dimensions to provide an interactive executive view.

## 2. Objectives

1. Consolidate retail performance information into a structured analytical data model.
2. Create reusable DAX measures for business KPIs.
3. Compare actual sales with targets.
4. Identify leading and underperforming regions, categories, channels, and sales representatives.
5. Analyze monthly trends and product returns.
6. Present findings in an executive dashboard that can be filtered interactively.

## 3. Data model

The model includes the following tables:

| Table | Purpose |
|---|---|
| FactSales | Transaction-level sales data |
| FactReturns | Returned-unit and refund information |
| FactTargets | Sales targets by period, region, and category |
| DimDate | Calendar attributes for time analysis |
| DimCustomer | Customer attributes |
| DimProduct | Product and category attributes |
| DimStore | Store attributes |
| DimSalesRep | Sales representative attributes |
| DimChannel | Sales channel attributes |
| DimMonth | Month and year analysis |
| DimRegion | Region attributes |
| DimCategory | Product category attributes |

The model uses relationships between fact tables and their relevant dimensions. Dimension keys should be unique on the one side of each one-to-many relationship, with matching foreign keys on the many side.

## 4. Data preparation and validation

The project validation checks covered missing values, exact duplicates, duplicate primary keys, orphan foreign keys, invalid quantities, discount ranges, negative prices or sales, and calculation consistency.

The validation review found no missing values, exact duplicates, duplicate primary keys, orphan foreign keys, invalid quantities, discounts outside the expected range, negative prices or sales, or sales-calculation mismatches. Four negative-profit transaction lines were reviewed and retained as legitimate records.

## 5. Dashboard design

The Executive_Dashboard sheet contains four headline KPI cards:

- Total Sales
- Total Profit
- Profit Margin
- Target Achievement

It also contains six analytical charts:

1. Monthly Sales & Profit Trend
2. Regional Sales vs Target
3. Revenue by Product Category
4. Revenue Contribution by Channel
5. Top 5 Sales Representatives
6. Returned Units by Reason

Four slicers provide interactive filtering:

- Year
- Region
- Category
- Channel

The dashboard uses PivotTables and PivotCharts supported by the Power Pivot data model.

## 6. KPI definitions

| KPI | Meaning |
|---|---|
| Total Sales | Sum of sales revenue |
| Total Profit | Sum of profit |
| Profit Margin | Total Profit divided by Total Sales |
| Total Orders | Count of distinct orders |
| Total Units Sold | Sum of units sold |
| Average Order Value | Total Sales divided by Total Orders |
| Sales Target | Sum of target values in the current filter context |
| Target Achievement | Actual Sales divided by Sales Target |
| Returned Units | Sum of returned units |
| Return Rate | Returned Units divided by Units Sold |
| Refund Amount | Sum of refund amounts |
| Sales vs Target Variance | Actual Sales minus Sales Target |

The measures respond to the applicable filter context. For ratio measures, the denominator and filter context should be checked when interpreting results.

## 7. Overall model results

| Metric | Overall result |
|---|---:|
| Total Sales | ₦2,862,662,121.72 |
| Total Profit | ₦718,932,329.72 |
| Profit Margin | 25.11% |
| Total Orders | 7,800 |
| Total Units Sold | 18,740 |
| Average Order Value | ₦367,007.96 |
| Total Sales Target | ₦8,250,211,000.00 |
| Target Achievement | 34.70% |
| Total Returned Units | 710 |
| Return Rate | 3.79% |
| Total Refund Amount | ₦115,776,026.96 |
| Sales vs Target Variance | -₦5,387,548,878.28 |

These are full-dataset figures before slicer filtering.

## 8. How to interact with the dashboard

1. Open the workbook in Microsoft Excel.
2. Navigate to the Executive_Dashboard worksheet.
3. Select one or more values in the Year, Region, Category, or Channel slicers.
4. Review the updated KPI cards and charts.
5. Clear slicer selections to return to the full-dataset view.

## 9. Limitations and next steps

- The dashboard reflects the supplied dataset and its definitions; it should not be interpreted as live business reporting.
- Target achievement is below 100% overall in the current dataset.
- Add dashboard screenshots to the `images/` folder.
- Add the final Excel workbook to the `dashboard/` folder only after privacy review.
- Consider adding a short methodology note for any custom business rules used in the source data.

## 10. Privacy

Before sharing the workbook publicly, remove or anonymize personal customer information, sensitive transaction details, and confidential business data. Confirm that you have permission to publish the source data.
