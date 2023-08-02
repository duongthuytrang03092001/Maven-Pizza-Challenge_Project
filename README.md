# Project Name: "Maven Pizza Data Analysis Project: SQL & Power BI"
Maven Pizza Challenge, analytics with SQL Server, Power BI
# Specific skills and technologies used in the project: Data Cleaning by Power Query Editor, Power BI (DAX language) and Data Visualization in Power BI, SQL Server.
# Introducing the Maven Pizza Challenge
Link " https://mavenanalytics.io/blog/maven-pizza-challenge " 
# Project Overview:
- The purpose of the analysis: Analyze the pizza business project to shed light on the following questions:
+ What days and times do we tend to be busiest?
+ How many pizzas are we making during peak periods?
+ What are our best and worst-selling pizzas?
+ What's our average order value?
  
==> The insights you aim to gain from the dataset is to see the current situation of the store, understand the business situation and grasp
the advantages of the store to make suggestions to help promote store development, product consumption and increase store revenue.

**About the dataset**
This dataset contains 4 tables in CSV format_
1. The Orders table contains the date & time that all table orders were placed

 
|    Table      |      Field       |  Description     |
| :------------:|:-------------:|:-----:|
|    orders          |       order_id     |  Unique identifier for each order placed by a table   |
|     orders         |        date      |   Date the order was placed (entered into the system prior to cooking & serving)|  
|     orders         | time     |    Time the order was placed (entered into the system prior to cooking & serving)|
  

2. The Order Details table contains the different pizzas served with each order in the Orders table, and their quantities
    
|       Table       |      Field        | Description     |
| :------------:|:-------------:|:-----:|
|    order_details          |        order_details_id      |  Unique identifier for each pizza placed within each order (pizzas of the same type and size are kept in the same row, and the quantity increases) |
|     order_details         |        order_id      |   Foreign key that ties the details in each order to the order itself |  
|     order_details         | pizza_id             |  Foreign key that ties the pizza ordered to its details, like size and price|  
|     order_details         | quantity             |    Quantity ordered for each pizza of the same type and size |
  

3. The Pizzas table contains the size and price for each distinct pizza in the Order Details table, as well as its broader pizza type
    
|       Table       |      Field        | Description     |
| :------------:|:-------------:|:-----:|
|    pizzas         |     pizza_id|	Unique identifier for each pizza (constituted by its type and size) |
|     pizzas         |      pizza_type_id	| Foreign key that ties each pizza to its broader pizza type   |
|    pizzas         |size |	Size of the pizza (Small, Medium, Large, X Large, or XX Large) |
|    pizzas         | price	| Price of the pizza in USD  |

4. The Pizza Types table contains details on the pizza types in the Pizzas table, including their name as it appears on the menu, the category it falls under, and its list of ingredients

|       Table       |      Field        | Description     |
| :------------:|:-------------:|:-----:|
|    pizza_types  |   pizza_type_id|	Unique identifier for each pizza type |
|     pizza_types	|name|	Name of the pizza as shown in the menu  |
|    pizza_types	|category	|Category that the pizza fall under in the menu (Classic, Chicken, Supreme, or Veggie) |
|    pizza_types	|ingredients	|Comma-delimited ingredients used in the pizza as shown in the menu (they all include Mozzarella Cheese, even if not specified; and they all include Tomato Sauce, unless another sauce is specified)  |


