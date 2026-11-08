# Customer Churn Analysis Dashboard | Power BI

## Project Overview
This project focuses on analyzing customer churn using Power BI. The dashboard helps understand customer behavior, identify churn patterns, and explore factors associated with customer retention.

## Dataset
- Total Records: 1,000 customers
- Total Columns: 10
- File: `customer_churn_data.csv`

## Tools Used
- Microsoft Power BI
- DAX
- CSV Dataset

## Dashboard Features
- Total Customers
- Churned Customers
- Churn Rate
- Average Monthly Charges
- Customer Churn by Contract Type
- Customer Churn by Internet Service
- Customer Distribution by Gender
- Customer Distribution by Age Group
- Interactive Contract Type Slicer

## Key DAX Measures

**Total Customers**
```dax
Total Customers = COUNTROWS('customer_churn_data')
```

**Churned Customers**
```dax
Churned Customers =
CALCULATE(
    COUNTROWS('customer_churn_data'),
    'customer_churn_data'[Churn] = "Yes"
)
```

**Churn Rate**
```dax
Churn Rate =
DIVIDE([Churned Customers], [Total Customers], 0)
```

**Average Monthly Charges**
```dax
Average Monthly Charges =
AVERAGE('customer_churn_data'[MonthlyCharges])
```

## Objective
To build an interactive and easy-to-understand dashboard that provides insights into customer churn and supports data-driven business decisions.

## Project Files
- Power BI dashboard (.pbix)
- Customer churn dataset (.csv)

## Author
Rosemaria Jose

Data Analytics | Power BI | SQL | Python
