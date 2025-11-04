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
1. What are the total sales, quantity, and average spent per order?
   The Total Sales across all 3 stores is **$698,812.33**, Quantity sold is **214,470**, and the Avg Order Value (AOV) is **$4.69**
2. What are the sales, quantity, and AOV in individual stores?
3. Which products are the top-selling products by revenue and quantity in each store?
4. What are the Top 5 slow-moving products
5. How is the unit price distributed
6. Which product category gives the highest margin
7. What are the Peak hours for coffee sales
8. How is the revenue trend from month to month over the 2 Quarters
9. Month-over-Month Growth
10. Which day of the week contributes the most to sales

### Visualiztion


### Summary And Recommendation




