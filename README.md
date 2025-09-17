# Company Revenue & Sales Overview Dashboard

## Project Overview 🚀
This project demonstrates a complete data analysis workflow, from handling messy, unstructured data to developing an interactive dashboard with actionable insights. The goal was to transform raw sales data into a clean, reliable format and then visualize key business metrics to help stakeholders understand sales performance and make data-driven decisions.

## The Problem: Messy Data 🤯
The initial dataset was inconsistent and challenging to use for analysis. Key issues included:

- Inconsistent capitalization and invisible extra spaces in the 'Region' column (e.g., 'north', 'WEST', 'east') caused issues when filtering the data.
- Missing values (null) in critical fields like "Revenue" and "Discount".
- Non-standardized product entries, such as "phon" and "headfone," which would have resulted in inaccurate product-level analysis.

<img width="1104" height="489" alt="messy data" src="https://github.com/user-attachments/assets/e16d684d-689f-4fd0-b769-446e15d4d2ba" />


## Data Transformation & Cleaning ( Power Query ) 🧼

- Removed outliers (Quantity >= 1000 ) because well i don't think someone actually bought 1000 TV it's more likely system error.
- Used the custom column feature to correct misspelled product names ("phon" => "phone") wich is neccessary for later analysis.
- Changed the "Region" column to a consistent format (e.g., all uppercase, no spaces) using fonctions like TRIM and UPPERCASE.
- I created a second query and filtered the data to include only products with unit price values, removing the other columns. I then refined it further to ensure each product appeared only once. After that, I merged this query with the first one (after deleting the unit price and revenue columns from the first), resulting in a third query that contained all sales with the correct unit prices. This made it easy to create a new 'Revenue' column by simply multiplying 'Unit Price' by 'Quantity'.

<img width="640" height="210" alt="data cleaning 22" src="https://github.com/user-attachments/assets/5808dce1-b76b-48a9-9864-dda635c65fac" />


<img width="1105" height="492" alt="cleaned data" src="https://github.com/user-attachments/assets/edbb1de1-ef4c-4e3f-b435-d4a5489b3adf" />


## Data Visualization & Insights 📊
The cleaned data was used to create a dynamic dashboard that provides a clear overview of the company's sales performance. The dashboard includes several key visualizations:

- **Revenue per Region**: A pie chart to quickly compare sales performance across different regions.
- **Best Selling Products**: A bar chart that identifies the top-performing products.
- **Monthly Revenue Trend**: A line chart that tracks sales over time, allowing for a quick analysis of seasonal or monthly trends.
- **Key Performance Indicators (KPIs)**: Simple cards displaying "Total Revenue" and "Monthly Revenue Average" for quick, at-a-glance information.

The dashboard includes interactive slicers for Date, Product, and Region, allowing users to filter the data and explore specific insights.

<img width="868" height="440" alt="dashboard" src="https://github.com/user-attachments/assets/4a3f3649-f4f5-41ad-9536-87163e5340f0" />

## Tools & Technologies Used 🛠️
- **Microsoft Excel**: For the core workbook.
- **Power Query**: The primary tool used for data extraction, cleaning, and transformation.
- **Pivot Table**: For building the data model and summarizing relationships between tables.
- **Pivot Chart**: For visualizing the summarized data.
