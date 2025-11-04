# Coffee_Sales_Performance_Analysis

### Project: Coffee Sales Performance Analysis

   The objective of this analysis is to check the financial health of a coffee brand that has 3 physical stores and look for where optimizations are needed for maximum profit from business settings. In this analysis, we walk through what the top performing stores, products, and categories are, and check if low price leads to an increase in quantity or sales, etc.... And at the end of the analysis, recommendations will be provided based on the analysis outcomes on business objectives (business questions).

#### Dataset And Data Dictionary:

This dataset is from kaggle.com between 6 months period (Jan - June 2023), it contains 11 columns(but will be reduce to columns needed to aid analysis tool performance) and approximately 150k records, due to this amount of data present we can assume that whatever the result of our analysis is, it can be use or aid in decision making for stakeholder(s).

**Columns present**:

- (Remove)
Store ID,
Product ID,
Product Details

- (Need)
Transaction Date,
Transaction Time,
Transaction Qty,
Store Location,
Unit Price,
Product Category,
Product Type

7 columns are needed for our analysis

[Analysis Notebook](https://github.com/Harbdulahi/Coffee_Sales_Performance_Analysis/blob/main/Coffee%20sales%20Performance/dataset%20and%20notebook/coffee_sale_performance_analysis.ipynb)

### Tools And Libraries
- Python
- Jupyter Notebook (VsCode)
- Pandas (Data Analysis Library)
- Matplotlib And Seaborn (Visualization)

### Key Steps
**Data Cleaning And Exploration** (Not EDA)
- Importing libraries
- Merging and converting date and time columns into a datetime object
- Creating calculated fields (sale, month, month_name, day_name, and hour)
- Checked and fixed duplicate records and null data points
- Dropped unnecessary column('store_id', 'product_id', 'product_detail') to improve tools performance.

### Business Questions and insights
1. **What are the total sales, quantity, and average spent per order?**
   
   The Total Sales across all 3 stores is **$698,812.33**, Quantity sold is **214,470**, and the Avg Order Value (AOV) is **$4.69**


2. **What are the sales, quantity, and AOV in individual stores?**
   | Store Location | Total_Sale | Transaction_Quantity	| Unique_Order_count	| Aov |
   |----------------|------------|-----------------------|--------------------|-----|
   |     Astoria    | 232243.91	|         70991	      |        50599	      |4.59 |
   | Hell's Kitchen | 236511.17  |         71737	      |        50735	      |4.66 |
   | Lower Manhattan	| 230057.25	|         71742	      |        47782	      | 4.81|

   ![KPIs across stores](https://github.com/Harbdulahi/Coffee_Sales_Performance_Analysis/blob/main/Coffee%20sales%20Performance/chart_and_tables/sales%2CQuantity%2COrdercount%2CandAOV.png)
   
   There is only *slight* variation among the 3 stores **KPIs**

 
3. **Which products are the top-selling products by quantity in each store?**

   | No. |Store Location|	Product Type	|Transaction Qty|
   |----|---------------|-----------------|---------------|
   |1	| Astoria	| Brewed Chai tea |	9306|
   |2	| Astoria	| Gourmet brewed coffee	|8938|
   |3	| Astoria	| Barista Espresso	|7345|
   |4	| Hell's Kitchen	| Barista Espresso	|9064|
   |5	| Hell's Kitchen	| Brewed Chai tea	|8755|
   |6	| Hell's Kitchen	| Gourmet brewed coffee	|8472|
   |7	| Lower Manhattan	| Gourmet brewed coffee	|8563|
   |8	| Lower Manhattan	| Barista Espresso	|8534|
   |9	| Lower Manhattan	| Brewed Chai tea	|8189|

   Among the 3 stores, **Brewed Chai tea** sold the most, and in Hell's Kitchen, **Barista Espresso** sold the most. While in Lower Manhattan **Gourmet Brewed Coffee** Sold the Most. Despite different stores having different top product there's consistency among the 3 top products been sold in each store location with slight margin among them. The 3 top product sold could likely be because they are low price product. 

   "Checking average unit price of each product to verify if low unitprice leads to increase in quantity sold"
      |Product_type|	unit_price| Quantity |
      |------------|----------------|-----------|
      |Barista Espresso| 3.65| 24943 |
      |Brewed Chai tea| 2.93| 26250 |
      |Gourmet brewed coffee | 2.69| 25973 

      Yes low selling unit price leads to increase in overall quantity sold (not per row or data point)


4. **What are the Top 5 slow-moving products**

   |Product	|Quantity Sold| Unit price|
   |---------|------------|-----------|
   |Green beans|	134 | 10.00|
   |Green tea|	159	|9.25|
   |House blend Beans | 183 | 18.00|
   |Organic Chocolate | 221 | 7.60|
   |Clothing | 221 | 27.88|

   They are slow movers due to been slightly expensive than other products

   [Analysis Notebook](https://github.com/Harbdulahi/Coffee_Sales_Performance_Analysis/blob/main/Coffee%20sales%20Performance/dataset%20and%20notebook/coffee_sale_performance_analysis.ipynb)

5. **How is the unit price distributed**

   ![unit price distribution](https://github.com/Harbdulahi/Coffee_Sales_Performance_Analysis/blob/main/Coffee%20sales%20Performance/chart_and_tables/Unit_Price_Distribution.png)

   The distribution is **right skewed** meaning low price products sell the most

   
7. **Which product category gives the highest margin**

    |Category | Sale | Percentage|
    |---------|------|-----------|
    |Coffee  |269952.45| 38.6%|
    |Tea|  196405.95 |  28.10%|
    |Bakery| 82315.64  | 11.77%|
    |Drinking Chocolate|   72416.00 | 10.36%|
    |Coffee beans|  40085.25  | 5.73%|
    |Branded  |13607.00  |  1.94%|
    |Loose Tea |  11213.60  |  1.60%|
    |Flavours  |  8408.80  |  1.20%|
    |Packaged Chocolate |  4407.64 | 0.63%|


   ![category sales share](https://github.com/Harbdulahi/Coffee_Sales_Performance_Analysis/blob/main/Coffee%20sales%20Performance/chart_and_tables/category_sales_share.png)

    The **coffee category** give the highest sales margin of **38.63%**

8. **What are the Peak hours for coffee sales**
    
      **HOURS**
      |  6   | 7  |   8  |    9  |     10|       11  |      12   |  13     |  14  |   15|     16      |17       |18        |19      |20 |
      |------|----|------|-------|--------|--------|--------------|---------|-----|-----|--------------|---------|---------|---------|---|    
    |7811.95 |23579.90 |30579.85 |31014.85 |33297.10 |18188.15 |16162.90 |16620.95 |16725.35 |16737.05 |16861.55 |16527.65  |14241.20 | 10630.15 |973.85|

    ![hourly sale](https://github.com/Harbdulahi/Coffee_Sales_Performance_Analysis/blob/main/Coffee%20sales%20Performance/chart_and_tables/Hourly_Sales.png)

   The peak sales hour for coffee products is between **7am** and **10am**

9. **How is the revenue trend from month to month over the 2 Quarters**

   Sales has an upward trend with february having the least sales and june having the highest sales

![sales trend](https://github.com/Harbdulahi/Coffee_Sales_Performance_Analysis/blob/main/Coffee%20sales%20Performance/chart_and_tables/Sales_Trend_Across_The_Months.png)

10. **Month-over-Month Growth Rate**
  
   
    |Month |Growth_Rate (MOM) |
    |------|-------------------|
    |2023-01-31	| 0% |
    |2023-02-28	| -6.77% |
    |2023-03-31	|  29.79% |
    |2023-04-30	|  20.34% |
    |2023-05-31	| 31.76% |
    |2023-06-30	| 6.22% |
   
      The Avg growth rate across the months is: **16.27%**

12. **Which day of the week contributes the most to sales**
  
   ![weekday sale](https://github.com/Harbdulahi/Coffee_Sales_Performance_Analysis/blob/main/Coffee%20sales%20Performance/chart_and_tables/Weekly_Sales_Trend.png)
   
   There is almost no variation between the weekly sales, and Weekdays make more sales than weekend only by slight margin (almost no difference)

13. **What is the Product Category Sales Trend Across the Months Like**

    ![category sales trend](https://github.com/Harbdulahi/Coffee_Sales_Performance_Analysis/blob/main/Coffee%20sales%20Performance/chart_and_tables/Category_Sales_Trend_Across_the_Month.png)

    [Analysis Notebook](https://github.com/Harbdulahi/Coffee_Sales_Performance_Analysis/blob/main/Coffee%20sales%20Performance/dataset%20and%20notebook/coffee_sale_performance_analysis.ipynb)

### Other Visuals

Top Expensive and bottom 3 affordable product (Unit price)

![topandbottom3](https://github.com/Harbdulahi/Coffee_Sales_Performance_Analysis/blob/main/Coffee%20sales%20Performance/chart_and_tables/Top_3_Bottom_3_products_(Avg_Unit_Price).png)

Sales by Product Category
![category_sales](https://github.com/Harbdulahi/Coffee_Sales_Performance_Analysis/blob/main/Coffee%20sales%20Performance/chart_and_tables/Sales_by_Product_Category.png)

Unit price vs quantity correlation 

![correlation](https://github.com/Harbdulahi/Coffee_Sales_Performance_Analysis/blob/main/Coffee%20sales%20Performance/chart_and_tables/Unit_Price_Vs_Quantity_Sold_Correlation.png)

### Summary And Recommendation

After completing the sales analysis we can say that coffee, tea and bakery category contribute to the overall sales. There is an upward trend in sales across the 6 months period with February having the least sale and June, the peak sale.

There's almost no correlation between unit price and quantity sold by row level, ẹ.g if coffee is $3.4 there's no increase in quantity for that record (quantity frequency distribution will be right skew, customer purchase 1 or 2 product(s) per order at least)

The Sales across all 3 stores are consistence, with almost no difference in revenue generated.

The coffee, tea and bakery category has the highest sales trend across 6 month, the MoM on average across the 6 month period is at 16.27%

There's almost no change between weekdays and weekends sales(slight variation)


### Recommendation

Discount can be offer on expensive product category during the rush hours (7am - 10am) to increase revenue.




[Analysis Notebook](https://github.com/Harbdulahi/Coffee_Sales_Performance_Analysis/blob/main/Coffee%20sales%20Performance/dataset%20and%20notebook/coffee_sale_performance_analysis.ipynb)


