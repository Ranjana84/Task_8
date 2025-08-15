# Task 8 - Simple Sales Dashboard

This project is part of the Data Analyst Internship Task 8.

## Objective
Create a basic interactive dashboard that shows sales performance by product category, region, and month using the **Sample - Superstore** dataset.

## Steps Followed (1–6)
1. **Imported Dataset**  
   Loaded `Sample - Superstore.xls` file into Power BI.

2. **Created Month-Year Field**  
   - Added a calculated column in DAX:
     ```DAX
     Month-Year = FORMAT('Sample - Superstore'[Order Date], "MMM-YYYY")
     ```
   - Created a sorting column:
     ```DAX
     MonthStart = DATE(YEAR('Sample - Superstore'[Order Date]), MONTH('Sample - Superstore'[Order Date]), 1)
     ```
   - Sorted Month-Year by MonthStart for correct chronological order.

3. **Created Visuals**  
   - **Line Chart**: Sales over Months  
   - **Bar Chart**: Sales by Region  
   - **Donut Chart**: Sales by Category  

4. **Added Slicer**  
   Added slicer for Region to make the dashboard interactive.

5. **Highlighted Top Performers**  
   Applied conditional formatting on charts to highlight regions and categories with higher sales.

6. **Insights**  
   - West region recorded the highest sales, followed by East and Central.  
   - Technology category contributed the largest share of sales, followed by Furniture and Office Supplies.  
   - The total sales in the dataset were approximately **$2.89M**.  
   - The sales trend shows an overall upward movement with noticeable peaks in certain months.

## Files in Repository
- `task8_dashboard.pbix` – Power BI dashboard file  
- `Task8_Insights.pdf` – Screenshot with insights  
- `README.md` – Project documentation  

## Tools Used
- Power BI Desktop
- DAX for calculated fields

## Author
Ranjana Chaursiya
