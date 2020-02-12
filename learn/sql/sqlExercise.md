---
title: SQL Exercise
date: '2-12-2020'
module: newSQL
order: 1
---

## SQL Exercise Using bestbuy database

-- find all products--
SELECT * FROM BestBuy.Products;

* find all products that cost $1400

* find all products that cost 11.99 or 13.99

* find all products that do NOT cost 11.99 - using NOT

* find  all products and sort them by price from greatest to least

* find all employees who don't have a middle initial

* find distinct product prices

* find all employees whose first name starts with a j

* find all Macbooks --

* find all products that are on sale

* find the average price of all products --

* find all Geek Squad employees who don't have a middle initial --

* find all products from the products table order by Price descending

--------------------------------------------------------------------------------------------------

* joins: select all the computers from the products table:
  * using the products table and the categories table, return the product name and the category name

* joins: find all product names, product prices, and products ratings that have a rating of 5

* joins: find the employee with the most total quantity sold.  use the sum() function and group by

--------------------------------------------------------------------------------------------------

* joins: find the name of the department, and the name of the category for Appliances and Games

* joins: find the name, total # sold, and total price sold,
for Eagles: Hotel California --You may need to use COUNT() && SUM()

* joins: find Product name, reviewer name, rating, and comment on the Visio TV. (only return the items above for the lowest rating!)

-------------------------------------------- Extra - May be difficult
/* Your goal is to write a query that serves as an employee sales report.
This query should return the employeeID, the employee's first and last name, the name of each product, how many of that product they sold and what date they sold it on */
