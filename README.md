# Plato-Pizza-Report

### Project Overview

The primary objective of the Plato Pizza Report is to analyze sales and customer data to derive actionable insights that can help improve business strategies, optimize operations, and enhance customer satisfaction for Plato Pizza.

### Data Sources
This dataset contains 4 tables in CSV format.

-The Orders table contains the date & time that all table orders were 
placed.

-The Order Details table contains the different pizzas served with each 
order in the Orders table, and their quantities.

-The Pizzas table contains the size and price for each distinct pizza in the 
Order Details table, as well as its broader pizza type.

-The Pizza Types table contains details on the pizza types in the Pizzas 
table, including their name as it appears on the menu, the category it falls 
under, and its list of ingredients

### Tools
- Microsoft Power BI Desktop[Download Here](https://powerbi.microsoft.com/en-us/downloads)

### Data Cleaning And Preparation
In the intial Data Preparation phase, I performed the following;
1. Data loading and Inspection
2. Data Modelling Techniques which incudes; Creating relationships/cardinality, Calculated columns and measures
3. Data Formatting 

### Exploratory Data Analysis
EDA involved exploring the Sales data to answer the key questions, such as;
- What days and times do we tend to be busiest?
- What are our best and worst selling pizzas?
- What's our average order value?
- How much money did we make this year? Can we identify any 
seasonality in the sales?

### Data Analysis
Includes some intresting functions and syntax used in creating measures;

``` DAX
Average Order Value = AVERAGEX(SUMMARIZE(orders,orders[order_id],"orderValue", [Total Order Value]),
[orderValue])
```
```DAX
 Total Order Value = SUMX(order_details,order_details[quantity] * RELATED(pizzas[price])) 
```
```DAX
Total Pizza Sales = SUM(order_details[quantity]) 
```
### Results And Findings
- Weekly sales peaked between Fridays(total of 3,538 orders), Thursdays(3,239 orders), Saturday(3,158 orders). Also, the busiest times during these days of the week are: Fridays(around 12.55pm, lunch time), Saturdays(Around 6.00pm), and Thurdsays(12.55pm)

- The best selling Pizzas was the Thai Chicken Pizza and the worst selling Pizza was the The Brie Carrie Pizza

- The Average Order Value was $38
- The total Revenue generated was $817,860, with the revenue peaking highest in the month of July at $72,560.





