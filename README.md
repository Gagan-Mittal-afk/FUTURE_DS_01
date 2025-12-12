E-Commerce Sales Performance Dashboard – Power BI

A comprehensive business intelligence project analyzing sales trends, product performance, customer insights, and revenue drivers.

 Project Overview

This project presents an interactive Power BI dashboard developed to analyze e-commerce sales data and uncover meaningful insights for informed business decision-making.
The dashboard provides a multi-dimensional view of:

1.	Best-selling products
2.	Monthly & yearly sales trends
3.	High-revenue categories
4.	Profitability insights
5.	Customer & regional performance
6.	Business opportunities and recommendations

This project demonstrates practical skills in data analysis, DAX, visualization design, and business storytelling, making it ideal for business stakeholders and data-driven teams.

Dataset Description

The dataset used in this project was sourced from Kaggle and contains typical e-commerce transaction-level records, including:

🔹 Key Columns in the Dataset

1.	Order ID
2.	Order Date
3.	Ship Date
4.	Product ID
5.	Product Name
6.	Category / Sub-Category
7.	Quantity
8.	Unit Price
9.	Sales
10.	Profit
11.	Discount
12.	Customer Details
13.	Region / City / State

The dataset consists of thousands of rows representing real-world transactional behavior.

Data Cleaning & Transformation (Power Query)

Data preparation is a critical part of the project. The following steps were performed in Power Query before loading the model:

 1. Data Type Corrections

1.	Converted dates to Date type
2.	Converted Sales, Profit, Discount to Decimal Number
3.	Converted Quantity to Whole Number
4.	Set Category, Product Name, Region as Text




 2. Handling Missing Values

1.	Replaced null numeric values (Sales, Profit, Quantity) with 0
2.	Replaced null text fields with "Unknown"

 3. Removing Duplicates

Ensured Order ID + Product ID combinations were unique

 4. Creating Calculated Columns

1.	A key calculated column added was:
2.	Total Sales = Quantity × Unit Price
3.	This ensured accurate sales contribution per product line.

 Data Modeling

1.	A Star Schema-style approach was followed:
2.	Fact Table: Sales/Orders dataset
3.	Dimension Tables: Products, Customers, Regions (if available)
4.	Relationships were created using:
5.	Product ID
6.	Customer ID
7.	Region/State fields

This structure improves slicing, filtering, and visual performance.



DAX Measures Created

To enhance analysis, several DAX measures were created:

Total Sales
Total Sales = SUM('Data'[Total Sales])

 Total Quantity Sold
Total Quantity = SUM('Data'[Quantity])

 Total Profit
Total Profit = SUM('Data'[Profit])

 Total Orders
Total Orders = DISTINCTCOUNT('Data'[Order ID])

 Sales Trend (Month/Year)
Sales Trend = CALCULATE([Total Sales], ALLEXCEPT('Data', 'Data'[Order Date]))

 Best-Selling Product
Top Product = 
CALCULATE([Total Sales], 
TOPN(1, ALL('Data'[Product Name]), [Total Sales], DESC))

These measures power the dynamic visuals in the dashboard.

 Dashboard Design & Visuals

The dashboard consists of three interactive pages, each designed with clear business objectives in mind.

 Page 1: Sales Overview Dashboard

This page gives a high-level business summary.

 Key Visuals:

1.	KPI Cards:
2.	Total Sales
3.	Total Profit
4.	Total Orders
5.	Total Quantity Sold
6.	Line Chart:
7.	Monthly/Yearly Sales Trend
8.	Identifies peak periods, seasonal patterns
9.	Bar Chart – Sales by Category
10.	Shows which product categories generate the highest revenue
11.	Donut Chart – Quantity Sold by Category
12.	Reveals customer purchasing behavior across categories

This page answers:

“How are we performing overall, and what are the main revenue drivers?”

Page 2: Product Performance Analysis

This page focuses on understanding which products contribute most to revenue and profit.

 Key Visuals:

1.	Top 10 Best-Selling Products (Bar Chart)
2.	Product Profitability Scatter Plot (Sales vs Profit)
3.	Segment-wise Product Sales Breakdown
4.	Product Table with Sales, Quantity, Profit

This page answers:

“Which products should we promote, discount, or discontinue?”

 Page 3: Customer & Regional Insights

This page explores customer behavior and geographic performance.

 Key Visuals:

1.	Sales by Region (Bar Chart)
2.	Map Visual – Revenue by State/City
3.	Top Customers by Revenue
4.	Customer Segment Visuals

This page helps identify:

“Where do our most valuable customers come from?”
“Which regions offer expansion opportunities?”

Key Business Insights

Based on dashboard analysis:
 1. Top-performing categories drive a large portion of revenue
Certain categories consistently outperform, suggesting strong customer demand.
 2. A few products contribute disproportionately to total sales
This follows the Pareto principle (80/20 rule)
 3. Seasonal trends show peak sales in specific months
Helps plan inventory, staffing, and marketing campaigns
 4. High-profit but low-sales items show strong potential
These products are ideal candidates for targeted promotions.
 5. Geographic analysis reveals high-revenue regions
Businesses can focus logistics and marketing budgets accordingly.

 Skills Demonstrated

This project showcases proficiency in:

🔸 Power BI Desktop
🔸 Data Cleaning & Transformation with Power Query
🔸 DAX Calculations
🔸 Data Modeling
🔸 Dashboard Design & Visual Storytelling
🔸 Business Analytics & Insights
🔸 User-Centric Report Building

This aligns perfectly with real-world data analyst responsibilities.

Conclusion

This e-commerce dashboard provides a powerful and user-friendly analytical tool that helps stakeholders:

1.	Track real-time sales performance
2.	Identify growth opportunities
3.	Improve profitability
4.	Understand customer behavior
5.	Make data-driven business decisions

The project demonstrates the complete BI workflow from raw data → actionable insights.

 How to Use This Repository

1.	Download the .pbix file
2.	Open it in Power BI Desktop
3.	Interact with the filters, visuals, and reports
4.	Explore each page for detailed insights


 Author

Gagan Mittal
📧 mittalgagan2004@gmail.com

💼 Data Analyst | Power BI Developer | Business Intelligence Enthusiast
