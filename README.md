# Sales Performance Dashboard


## Problem Statement

This dashboard helps management understand customers better by visualizing their purchasing behaviors, preferences, and how they respond to different promotions and discounts. It also supports management in making more informed decisions about product strategies, marketing campaigns, and customer service improvements.

Sales data analysis helps management in several key ways by enabling informed, data-driven decision making and improving business outcomes:

Enhanced Decision-Making
Provides comprehensive visibility into product performance, customer trends, and sales channels, allowing leaders to identify which offerings and markets are driving growth and which need attention.​

Enables management to assess the impact of pricing, promotions, and discounts, making it easier to optimize revenue and profitability.​

Strategic Planning and Forecasting
Facilitates accurate sales forecasting, ensuring better resource allocation and inventory management while minimizing financial risks such as overstock or stockouts.​

Allows for the tracking of customer segments and buying behaviors, empowering management to tailor marketing and sales strategies to different audiences.​

Monitors goal achievement and progress, giving managers the ability to set realistic targets and adjust strategies based on data feedback.​

Resource Efficiency and Competitive Advantage
Supports more efficient use of time, budget, and personnel by pinpointing high-impact activities and eliminating underperforming approaches.​

Equips management with actionable insights to respond swiftly to changing market dynamics, securing a sustained competitive edge.


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 :  The initial dataset consisted of four tables: Dim Customers, Dim Products, Dim Promotions, and a Fact Table. Each table was profiled and transformed using Power BI’s robust features to enhance data integrity and analytic precision.
- Step 4 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 5 : Dim Customers: Examined each column for data types and value consistency. The Customer ID column was validated to have unique and distinct values, confirming its suitability as a primary key. All columns were checked and corrected for proper data types to facilitate accurate joins and reporting.
- Step 6 : Dim Products: Reviewed product details, ensuring Product ID was unique and set as a primary key. All column types were standardized, focusing on accuracy for analytic operations and seamless relationship modeling.
- Step 7 : Dim Promotions: Profiled all columns, establishing Promotion ID as a text-based primary key, since mathematical operations would not be performed on this field. Notably, the table lacked numerical values for "off" amounts. A new column was created using Power Query’s conditional column feature to derive a numeric “off percentage” for analysis.
- Step 8 : Fact Table: Served as the core sales data source and required extensive cleaning:

Null values were detected in Price Per Unit, Total Sales, Discount Percentage, and Net Sales fields.

Price Per Unit data was merged from the Dim Products table with the help of "Merge Queries" function, then multiplied by Units Sold to calculate Total Sales.​

Discount Percentage and Net Sales were resolved by joining with Dim Promotions, calculating discount amounts, and then computing Net Sales by subtracting the discount from the total.​

All joins and merges were validated to maintain data consistency and avoid introducing errors.

Relationships were established as one-to-many using each dimension’s primary key as foreign keys in the fact table.
- Step 9 : Problem Statement, KPIs for the same and chart used.

<img width="1064" height="281" alt="image" src="https://github.com/user-attachments/assets/d1c4b237-e26e-471e-9ec2-0dae7aae63a8" />



![Snap_1]<img width="1918" height="976" alt="Image" src="https://github.com/user-attachments/assets/dab6b01f-e8f8-4a04-82ad-7f0237e435b1" />
      

![Snap_2]<img width="1917" height="971" alt="Image" src="https://github.com/user-attachments/assets/83f56625-5c32-44b8-8d01-5d4823b2ea69" />


![Snap_3]<img width="1917" height="972" alt="Image" src="https://github.com/user-attachments/assets/cfc16144-ed8f-40fe-a8e8-d9b8714a7903" />
 

# Insights

A Three page report was created on Power BI Desktop.

Following inferences can be drawn from the dashboard;

### [1] Product Performance

   The top 5 products by sales, profit, or quantity sold are driving the largest portion of revenue, while the bottom 5 may require strategic attention, such as marketing boosts or discontinuation.
           
### [2] Sales Trends Over Time

Analysis of net sales by periods (daily, monthly, quarterly, annually) uncovers seasonal patterns, peak demand times, and possible downturns in business activity, allowing accurate forecasting and inventory planning.
  
  ### [3] Profit and Sales Relationship 
  
The scatter plot of profit versus net sales reveals the correlation between sales and profitability, highlighting products or categories that contribute high revenue but low profit margins, which may signal inefficiencies or pricing issues.

 ### [4] Comparative Analysis by Periods
 Comparing metrics between any two selected time periods uncovers changes in performance, identifies the impact of campaigns or market changes, and helps track progress against targets

 
 ### [5] Customer Acquisition and Retention
Discounts offered by specific promotions can attract new customers or retain existing ones, but a large share of revenue from discounted deals suggests potential over-reliance on discounts to drive sales.
 

 ### [6] Effectiveness of Promotions
 By comparing average discount values across various promotions, the business can identify which campaigns are most effective in driving profitable sales and which may attract price-sensitive, low-value customers.​

Promotions delivering higher customer lifetime value (CLV) and repeat business are preferable to those attracting only one-time buyers.

 ### [7] Geographic Sales Distribution
 Visualizing net sales by city on a map pinpoints high-performing regions and underperforming markets, guiding local marketing and resource allocation.

