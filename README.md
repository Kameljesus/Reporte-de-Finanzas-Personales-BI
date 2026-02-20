# 💰 Personal Finance Dashboard – Business Intelligence

🎯 Interactive financial performance dashboard designed to monitor personal financial indicators and support data-driven decision making.

🔗 Live Report:

https://app.powerbi.com/view?r=eyJrIjoiM2M1ZTYyZWItMjE3Yy00ZTM5LTlhMzktNDM1YzQ4YTk2ODQ3IiwidCI6ImFhNTFlOGMyLTU3ZjgtNGJiZC1hNjExLTA5MGIxYTFlODk0YyIsImMiOjR9&pageName=eb0625753c2ef28e0340

## 📊 Project Overview
Business Intelligence project developed in Power BI to visualize and analyze key personal finance indicators through interactive dashboards optimized for desktop, tablet, and mobile devices.

The report enables users to monitor:
- Total Income
- Total Expenses
- Net Profit (Utility)
- Cumulative Balance
- Income Goals Tracking
- Expense Budget Control
- Financial Projections

The solution includes structured relational data modeling, advanced DAX measures, and optimized data transformation using Power Query to improve performance and maintain a clean semantic model.

## 📈 Data Modeling & DAX Logic

The project implements:

- Optimized relational data model
- Data transformation and cleaning with Power Query (ETL process)
- Strategic column hiding for semantic clarity
- Advanced DAX calculations with context manipulation
- Dynamic cumulative measures (running totals)

```DAX
Balance = 
CALCULATE(
    [Net Profit], 
    FILTER(
        ALL(Finance), 
        Finance[Date] <= MAX(Finance[Date])
    )
)
```

This measure leverages `CALCULATE`, `FILTER`, and `ALL` to override filter context and dynamically compute a running balance over time.

## 🗂️ Analysis Dimensions

- Date
- Transaction Type (Income / Expense)
- Financial Category
- Goals
- Budgets
- Projections

## 🛠️ Technologies Used

- Power BI
- DAX (Data Analysis Expressions)
- Power Query (ETL)
- Relational Data Modeling
- Data Visualization
- Financial Analytics

## 📁 Report File

- `Proyecto4 - Finanzas Personales.pbix`
> Power BI Desktop is required to open the report file.
