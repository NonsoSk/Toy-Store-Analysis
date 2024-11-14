# Toy-Store-Analysis

![Background Main](https://github.com/user-attachments/assets/de33a42f-2fba-4a6b-94bd-98e2c75ef8d8)


## Introduction
 
This Power BI project is built around a business dataset to uncover key performance insights. It is particularly an analysis of a toy shop sales dataset. The project focuses on metrics like revenue and operational performance by tracking sales, profitability, and customer engagement across product categories and regions.

The goal of the project is to create an easy-to-use Power BI dashboard for business leaders, which will help them to quickly see trends in sales, product performance, and customer segments across different regions. This will allow them to make smart, data-driven decisions for growth and profitability.


## Problem Statement

We shall create an interractive dashboard inorder to simplify tracking important business metrics (KPIs), including:
- Sales trends and profit margins over time.
- How different products and categories perform.
- How regions and customer segments impact overall KPIs.

Generally, the dashboard would be designed to answer essential questions about key business areas and to reveal opportunities for improvement in sales and customer engagement.

## Overview of the Approach

The Power BI dashboard was built with features that make it both powerful and user-friendly:

- **Metric Aggregation:** which shows key metrics like total sales, profit, and regional performance in an easy-to-understand way.

- **Dynamic Filtering:** Interactive filters (slicers) which allows users view data by date, product category, and region.

- **Data Visualization:** Used visuals like line charts and bar charts to make it easy to spot trends and compare performance over time.

Moving forward, I demonstrated the following skills: 

- **Data Modeling:** Created links between tables for consistency and to make calculations across different dimensions accurate.

- **DAX Functions:** Used DAX to create custom calculations like year-over-year sales growth and profit margins.

- **Power Query Transformation:** Cleaned and structured data by removing duplicates and standardizing formats for smooth analysis.

## Data Modeling and Profiling
To understand how we modelled our data, let us first consider the tables we worked with:
- Calendar
- Products
- Inventory
- Sales
- Stores
  
The following relationships were created:

- Sales Table to Products Table: Joined on “Product_ID” to bring in product details for each sale.

- Sales Table to Stores Table: Linked via “Store_ID” to allow analysis by store location and region.

- Sales Table to Calendar Table: Linked on “Date” to analyze sales data by day, month, quarter, and year.

- Inventory Table to Products Table: Linked on “Product_ID” to match inventory levels to each product.

- Inventory Table to Stores Table: Linked on “Store_ID” to analyze stock by location.

In profiling the data, I discovered that 

1) There are 5 different category of products enabling segmentation of sales by category and then with 35 products
2) There are 29 unique cities, helping to analyze regional performance and Four (4) location types aid in assessing store performance by location type.

I went on to add additional Calculated Columns which includes Year, Month, Quarter, and Day to support aggregated time-based analysis.

## Data Transformations and Cleaning

The data underwent cleaning to enhance reliability and analytical accuracy. Here’s a breakdown of steps taken:

Removed Duplicates: Eliminated any duplicate entries based on unique identifiers (e.g., Sales ID or Product ID).

Handled Null Values: Replaced or removed rows with null values in critical columns like Sales Amount or Date, as they are essential for trend analysis.

Standardized Formats: Ensured date formats were consistent to avoid aggregation issues.

Filtering Outliers: Reviewed extreme sales and profit values to remove any entries that might distort insights.

Currency Conversion: Product cost and price values were likely converted to numeric formats.

Filtering for Valid Data: Ensures that only complete, relevant records (e.g., non-null Store_ID and Product_ID) are used.

## Dashboard Analysis and Insights

After this, I proceeded to analyzing my data so as to reveal business trends, understand product and category performance, and analyze customer behavior across different regions. Here’s a breakdown of each key metric, the visualization used, and the insights they provide to help guide strategic decisions.

The “General Sales Information”  page of our dashboard provides a comprehensive overview of the sales performance for a toy store chain. 

<img width="717" alt="General dashboard" src="https://github.com/user-attachments/assets/b7ed37ff-1090-4f55-9a4c-8b0b88781301">

The dashboard includes key performance indicators (KPIs) like total sales, total profit, and total revenue, along with product-specific and store-related insights. The aim is to give stakeholders a quick snapshot of the sales metrics, identify top-performing products, and analyze daily sales patterns.

You can interact with the dashboard [**HERE**](https://app.powerbi.com/view?r=eyJrIjoiY2I0ODk4MzQtM2E4MC00ZDcwLThlNWYtZDAwYjVkYzVkOTRjIiwidCI6ImY4NzNhMzA5LTg2ZjgtNDg4OS05OTcxLTEzMDQwNDM0NjZmNCJ9)

However, the following insights were uncovered.

**KPI Cards:**

<img width="460" alt="KPI`S" src="https://github.com/user-attachments/assets/200ff6cc-a2e4-4d7d-b28b-11ccb2553abe">

**Total Sales Metric**

The KPI displays the total number of units sold as 1.1 million across all stores, providing a quick view of overall sales volume and suggests a strong demand for products.

**Total Profit Metric**

This KPI provides an overview of profitability, showing the net earnings ($4M) from sales

**Total Revenue Metric**
 
This metric highlights the gross revenue, showing the total sales amount generated ($14.4M).
  
**Number of Stores**

There are 50 stores location in operation. Operating 50 stores implies a significant presence, possibly in multiple regions, allowing for a wider customer base. 

Number of Products: As seen, there are 35 different products being tracked.This relatively small number of products indicates a focused inventory, which might aid in operational efficiency and targeted marketing.

These KPIs give a high-level summary of the overall performance, indicating healthy sales and profitability across a significant number of stores and products.

Let`s consider other visuals.
In the Quantity Sold per Day Chart, we used the line chart  to visualize the  daily sales volume trends, showing fluctuations in quantity sold across the week.

<img width="328" alt="Qantity sold per day" src="https://github.com/user-attachments/assets/3a65da46-e57e-4d36-80d5-7a93d25c5f1c">

Here, we can notice that sales volume fluctuates throughout the week, with a steady increase from Monday to Saturday, but with Friday and Saturday having the highest sales (212K and 219K units respectively), which indicates a peak in demand and could likely be due to weekend shopping trends, while Sunday sees a significant drop (130K units).
This pattern of trend suggests that the store experiences the highest foot traffic towards the weekend, especially on Saturdays, with demand dropping off on Sundays and into the start of the week.

Moving forward, we can see the Top 5 Highest Sold Products. 
The essence of the visual is to help us understand which items drive the most volume.

<img width="284" alt="Highest sold product" src="https://github.com/user-attachments/assets/5b82a330-3dbf-464d-bb94-49fd5e4d49e6">

From the visual, it is evident that "Colorbuds" and "PlayDoh Can" are the highest sold products at 104K and 103K units respectively, with "Barrel O' Slime" at 92K, "Deck of Cards" at 84K, and "Magic Sand" at 61K following suit.
These figures indicate that arts and crafts-related toys like "Colorbuds" and "PlayDoh Can" are particularly popular, suggesting a potential trend or preference among customers for hands-on or creative toys.

We went on to examine the least sold products, with the aim of highlighting possible inventory challenges or unpopular items.

<img width="295" alt="Least product" src="https://github.com/user-attachments/assets/1e2fbe81-b2cc-4f54-9509-f1b1c20b5cb0">

The visual shows that "Mini Basketball Hoop" has the lowest sales at 2.6K, followed by "Uno Card Game" at 2.7K, and down to "Playfoam" at 4.2K. What this means is that classic board games and less interactive items are the least demanded products, which could be as a result of changing customer preferences or competition from digital alternatives. On another note, it could be that the products may not have been marketed effectively.


Having examined the first page of our dashboard, we shall have move to the "Start of Month Information" page which provides monthly summaries for orders, revenue, and profit and also helps stakeholders evaluate month-over-month performance and identify peak sales periods as can be seen below:

<img width="606" alt="Start of Month Info" src="https://github.com/user-attachments/assets/d02c0371-8fec-4c0c-9f62-1a794fbdede3">


Firstly, looking at the “Total Orders by Product Category” visual, we can see that the "Toys" and "Art & Crafts" categories of products are the top-selling with 221K orders each, followed by "Games" (157K), "Sports & Outdoors" (131K), and "Electronics" (99K). 

<img width="298" alt="Order by category" src="https://github.com/user-attachments/assets/125275d8-38dc-4a8e-be00-d4fcdc74fdb9">

This suggests that traditional toy items and creative products are popular among customers. Which is also a resonates with of our initial analysis that arts and crafts-related toys are the most demanded.

Our next analysis will be on “the total revenue by start of month” visual.

<img width="367" alt="Total Revenue by start of Month" src="https://github.com/user-attachments/assets/d7fc2f6c-849a-4fe9-9cdb-ddb7e390ae9d">

This visual shows revenue trends by the start of each month over time, giving a sense of revenue performance at the beginning of each month across the year.
From the visual, it is very clear that the peaks in revenue are Dec 2022 and March 2023, having total revenue as $877K and $884K respectively. This could possibly be due to seasonal demand (Maybe Christmas in Dec. and Easter in March). However, the month with the least revenue at the beginning of the month is Aug 2022 with $489K revenue generated. This could be because of the rainy season.



## Conclusion

This Power BI project provides clear insights into toy store sales, revealing top products, regional performance, and seasonal trends. Keeping stock of popular items, promoting lower sellers, and timing promotions for peak seasons and weekends can fuel growth. It’s all about using data-driven decisions to boost sales and profitability.

## Recommendation
Having analyzed the sales data properly, below are my recommendations for the Toy shop management.

1) For low sales products, evaluate the products for potential discontinuation, or consider running targeted promotions to boost sales. Discounts or bundle offers can be introduced for low-selling products like **Mini Basketball Hoops** to boost their sales. For example, offer a discount on "Mini Basketball Hoop" when purchased with a popular item like "Colorbuds." 

2) Analyzing customer feedback could provide insights into why these items aren’t performing well.

3) Analyze the reasons behind revenue spikes in specific months (Dec and March) and then  leverage holiday promotions, bundling, or limited-time offers. Finally, replicate successful strategies during similar periods. It would be nice also to Plan future campaigns around these high-revenue periods to maximize profit, potentially incorporating holiday themes or special events.

4) Explore why sales peak on certain days like Friday and Saturday. Promotions on slower days like Monday or Sunday could help balance demand. Weekly or monthly views of this trend could provide additional insights.

5) The discrepancy between Total profit and start-of-month profit suggests that start-of-month transactions may be less profitable or that higher-cost items sell more frequently later in the month. This pattern thus indicates potential differences in customer behavior throughout the month, where early purchases might be more cost-driven, and high-margin items could be purchased later. To this end, Investigate customer demographics and spending habits for start-of-month purchases versus mid-month purchases, and then implement targeted cross-selling or upselling strategies on higher-margin products in early-month transactions to boost profit.

6) Tailor product offerings, inventory levels, and marketing efforts based on store location type and time-based sales patterns to maximize location-specific performance.

7) Focus on maintaining adequate stock for high-demand products like “Colorbuds” and "PlayDoh Can" to avoid shortages.

8) Consider reducing inventory or re-evaluating the pricing strategy for low-performing products to optimize storage and reduce costs.

9) NYou can also reevaluate the positioning and display of least-sold products to improve visibility.

10) Consider targeted surveys or feedback collection to understand customer preferences better and tweak product offerings accordingly.


