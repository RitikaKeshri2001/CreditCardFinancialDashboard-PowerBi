# Credit Card Financial Dashboard using Power BI

## Project Overview
This project showcases a **Credit Card Financial Dashboard** built using Power BI, where data is sourced from PostgreSQL. The goal of the project is to provide insights into credit card transactions and customer information. The project includes two dynamic, real-time dashboards: **Credit Card Transaction Report** and **Credit Card Customer Report**.

The dashboards help visualize revenue, transaction counts, and other key metrics, enabling data-driven decision-making. Various filters, measures, and visualizations are incorporated to provide a comprehensive analysis of the data.

## Data Sources
- **CreditCard Table**: Contains fields such as `card_category`, `expenditure_type`, `client number`, `use_chip`, `total_transaction_amount`, `total_transaction_count`, `interest_earned`, etc.
- **Customer Table**: Contains fields like `client_num`, `customer_age`, `gender`, `customer_job`, `income`, etc.

## Data Cleaning & Transformation
Using **Power Query** in Power BI:
- Columns were added to the **CreditCard** table:
  - `week_num2`: Extracted from the string data in `week_num` (week numbers).
  - `revenue`: Calculated based on transaction amounts.
- Columns were added to the **Customer** table:
  - `AgeGroup`: Grouped customers by age using DAX.
  - `IncomeGroup`: Grouped customers by income level (low, mid, high) using DAX.

## Measures
Several DAX measures were created to calculate **week-on-week (WoW) changes** for key metrics:
- **Transaction Amount**
- **Customer Count**
- **Transaction Count**
- **Revenue**

These measures compare the current and previous week’s data, providing insights into weekly trends.

## Dashboards

### 1. Credit Card Transaction Dashboard
This dashboard provides a comprehensive analysis of credit card transactions. Key features include:
- **Visualizations**:
  - Revenue vs. `Expenditure Type`, `Customer Job`, `Education`, `Card Category`, `Transaction Mode`.
  - Line and stacked column chart: X-axis represents quarters, Y-axis shows revenue, and the line represents transaction count.
- **Table**:
  - Displays `card_category`, `revenue`, `transaction count`, `transaction amount`, and `interest earned`.
- **Filters**:
  - `Week_start_date`, `Quarter`, `Card_category`, `Gender`, `IncomeGroup`.
- **Cards**:
  - Key metrics such as total revenue, transaction count, transaction amount, and total interest earned.

### 2. Credit Card Customer Report
This dashboard focuses on customer demographics and their impact on revenue. Key features include:
- **Visualizations**:
  - Revenue vs. `Marital Status`, `Education`, `IncomeGroup`, `AgeGroup`, `Dependents`, and top 5 states, with `Gender` as the legend.
  - A line chart of revenue trends, also with `Gender` as the legend.
- **Table**:
  - Displays `Customer Job`, `Revenue`, `Interest Earned`, and `Income`.
- **Filters**:
  - `Week_start_date`, `Quarter`, `Card_category`, `Use_chip`, `Gender`.
- **Cards**:
  - Key metrics such as total revenue, interest earned, income, and customer satisfaction score.

##### Week 53 Insights
A detailed PowerPoint presentation is provided that highlights key insights from **Week 53**, based on the week-on-week analysis.

## Technologies Used
- **Power BI**: For data visualization and dashboard creation.
- **PostgreSQL**: For data storage and querying.
- **Power Query**: For data cleaning and transformation.
- **DAX**: For creating custom measures and calculations.

## How to Use This Project
1. Download the Power BI file (.pbix) from this repository.
2. Connect the Power BI report to your PostgreSQL database.
3. Ensure the data schema matches the **CreditCard** and **Customer** tables.
4. Review and interact with the dynamic dashboards to analyze credit card transaction data and customer insights.


