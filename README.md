# Retail Business Performance Dashboard

An interactive retail business intelligence project built with **Microsoft Excel, Power Pivot, DAX, PivotTables, PivotCharts, and slicers**. The dashboard is designed to help business stakeholders monitor sales performance, profitability, target achievement, product categories, sales channels, sales representatives, and product returns.

## Project overview

This project analyzes retail transactions from **January 2024 to December 2025** and presents the results in an executive dashboard. Interactive slicers allow users to explore performance by year, region, product category, and sales channel.

## Business questions

- How much revenue and profit did the business generate?
- What is the overall profit margin and average order value?
- How close is sales performance to the business target?
- Which regions and product categories contribute most to revenue?
- Which sales channels generate the most sales?
- Which sales representatives lead in revenue?
- How many units are returned, and what are the main return reasons?
- How does performance change over time?

## Dashboard features

- Executive KPI cards for Total Sales, Total Profit, Profit Margin, and Target Achievement
- Monthly sales and profit trend
- Regional sales versus target
- Revenue by product category
- Revenue contribution by channel
- Top five sales representatives
- Returned units by reason
- Interactive Year, Region, Category, and Channel slicers

## Data model

The Power Pivot model uses a star-schema approach with transaction and supporting dimension/target tables.

**Fact and target tables**
- `FactSales`
- `FactReturns`
- `FactTargets`

**Dimension tables**
- `DimDate`
- `DimCustomer`
- `DimProduct`
- `DimStore`
- `DimSalesRep`
- `DimChannel`
- Supporting month, region, and category dimensions

The model contains approximately **10,745 sales rows** and **498 return rows**.

## Selected overall results

The following are the validated overall results from the current project model. They represent the full dataset before applying interactive slicer filters.

| KPI | Result |
|---|---:|
| Total Sales | ₦2,862,662,121.72 |
| Total Profit | ₦718,932,329.72 |
| Profit Margin | 25.11% |
| Total Orders | 7,800 |
| Units Sold | 18,740 |
| Average Order Value | ₦367,007.96 |
| Sales Target | ₦8,250,211,000.00 |
| Target Achievement | 34.70% |
| Returned Units | 710 |
| Return Rate | 3.79% |
| Refund Amount | ₦115,776,026.96 |

## Key findings

- Electronics is the highest-revenue product category; Beauty & Personal Care is the lowest.
- The South West region records the highest sales.
- In-Store is the leading sales channel.
- Fatima Agu is the top sales representative by revenue (approximately ₦132.09 million).
- Emeka Akinola records the highest profit (approximately ₦43.63 million).
- No month in the reviewed period reached 100% of its sales target.

See [Project Documentation](docs/PROJECT_DOCUMENTATION.md) and [Business Insights](docs/BUSINESS_INSIGHTS.md) for more detail.

## Tools and skills demonstrated

- Microsoft Excel
- Power Pivot data modelling
- DAX measures and calculations
- Data cleaning and validation
- KPI development
- PivotTables and PivotCharts
- Interactive dashboard design
- Business analysis and insight communication

## Repository structure

```text
Retail-Business-Performance-Dashboard/
├── README.md
├── docs/
│   ├── PROJECT_DOCUMENTATION.md
│   └── BUSINESS_INSIGHTS.md
├── dashboard/
│   └── (Add the Excel workbook here)
└── images/
    └── (Add dashboard screenshots here)
```

## How to use

1. Download the Excel workbook from the `dashboard` folder once it is uploaded.
2. Open it in Microsoft Excel with Power Pivot support.
3. Use the Year, Region, Category, and Channel slicers to interact with the dashboard.
4. Review the KPI cards and charts to explore performance.

## Data privacy

Only publish data that you own or are authorized to share. Before uploading the workbook, confirm that customer names, contact details, transaction identifiers, and any other confidential information have been removed or anonymized. The summary figures in this README are aggregate project results.

## Project status

Documentation published. The Excel workbook and dashboard screenshots are to be added.

## Author

**Ogunkunle Goodness Feranmi**  
Aspiring Data Analyst | Excel | Power BI | DAX

- GitHub: [@Godspeedxreal](https://github.com/Godspeedxreal)
