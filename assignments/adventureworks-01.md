### **SQL Assignment: AdventureWorks Database**

#### **Instructions:** 
- Use SQL Server Management Studio (SSMS) connected to the AdventureWorks database.


### **Questions:**

<!-- #### **1. Basic Queries:** -->
1. Retrieve the list of all products, displaying `ProductID`, `Name`, `ProductNumber`, and `ListPrice`.
2. List all employees, including their `EmployeeID`, `JobTitle`, and `HireDate`.
3. Display all customers, showing `CustomerID`, `FirstName`, `LastName`, and `EmailAddress`.
4. Find all vendors, including `VendorID`, `Name`, and `CreditRating`.
5. Show all sales territories, including `TerritoryID`, `Name`, and `CountryRegionCode`.

<!-- #### **2. Filtering and Sorting:** -->
6. List all products with a `ListPrice` greater than $1000.
7. Retrieve all employees who were hired after January 1, 2010.
8. Find customers whose `LastName` starts with 'S'.
9. Show vendors with a `CreditRating` of 1 or 2, ordered by `Name`.
10. List all sales territories in the United States, ordered by `Name` alphabetically.

<!-- #### **3. Aggregate Functions:** -->
11. Calculate the average `ListPrice` of all products.
12. Find the total number of sales orders placed.
13. Determine the maximum `TotalDue` for any single sales order.
14. Calculate the sum of all `ListPrice` values for products in the "Bike" category.
15. Count the number of employees who have a `JobTitle` of 'Sales Representative'.

<!-- #### **4. Grouping and Aggregation:** -->
16. Group products by `ProductSubcategoryID` and find the average `ListPrice` for each group.
17. Group employees by `JobTitle` and count the number of employees in each title.
18. Find the total `TotalDue` for each customer, grouped by `CustomerID`.
19. Group sales orders by `TerritoryID` and find the sum of `TotalDue` for each territory.
20. List the number of products in each product category.

<!-- #### **5. Joining Tables:** -->
21. Retrieve a list of sales orders with `SalesOrderID`, `OrderDate`, and the customer’s `FirstName` and `LastName`.
22. List all employees along with their department names.
23. Find all products along with their subcategory and category names.
24. Display all purchase orders, including `PurchaseOrderID`, `OrderDate`, and the vendor’s `Name`.
25. List all products and their associated vendors.

<!-- #### **6. Advanced Joins:** -->
26. Find all customers who have never placed a sales order.
27. Retrieve products that have never been sold.
28. List employees who do not have any department history.
29. Show all vendors who have never supplied any products.
30. Find all sales territories that do not have any sales representatives assigned.

<!-- #### **7. Subqueries:** -->
31. Find the product with the highest `ListPrice`.
32. Retrieve the employee with the earliest `HireDate`.
33. List all customers who have placed more than 10 orders.
34. Find products that are more expensive than the average `ListPrice`.
35. Display all employees who earn more than the average salary in their department.

<!-- #### **8. Complex Queries:** -->
36. Retrieve the top 10 products by `ListPrice`.
37. Find the top 5 customers based on the total `TotalDue`.
38. List the top 3 most popular products by the number of times they were sold.
39. Retrieve the top 5 employees with the most sales.
40. Find the top 3 vendors by the total number of products supplied.

<!-- #### **9. Date and Time Functions:** -->
41. List all sales orders placed in the last 30 days.
42. Retrieve all employees who were hired in the last year.
43. Find all products that were added to the database in the last 6 months.
44. Show all purchase orders placed in the current year.
45. List all customers who have made a purchase in the last 90 days.

<!-- #### **10. String Functions:** -->
46. Display a list of all products with the `Name` in uppercase.
47. Find customers whose `EmailAddress` ends with 'adventure-works.com'.
48. List employees whose `FirstName` contains the letter 'A'.
49. Retrieve the first 5 characters of each product’s `ProductNumber`.
50. Concatenate the `FirstName` and `LastName` of all employees into a single column called `FullName`.
