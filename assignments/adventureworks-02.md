# SQL Server Assignment: DRL(SELECT)

## Instructions:
- Connect to the AdventureWorks database using SQL Server Management Studio (SSMS) or any other SQL environment.


### **Questions:**

<!-- ### 1. **LIKE Clause** -->
1. Retrieve all products whose name starts with 'Mountain'.
2. Find all customers whose last name ends with 'son'.
3. List all email addresses that contain 'adventure'.
4. Retrieve employees whose job title includes 'Manager'.
5. Find vendors whose name contains the word 'Bike'.
<!-- ### 2. **BETWEEN Clause** -->
6. List all products with a `ListPrice` between $500 and $1000.
7. Retrieve all sales orders placed between January 1, 2020, and December 31, 2020.
8. Find employees hired between January 1, 2015, and January 1, 2020.
9. List all purchase orders with a total due between $1000 and $5000.
10. Retrieve all customers with customer IDs between 10000 and 20000.
<!-- ### 3. **IN Clause** -->
11. Find all products in the 'Mountain-100' series.
12. List all customers who live in the states of 'CA', 'NY', and 'TX'.
13. Retrieve employees who have the job titles 'Sales Representative', 'Sales Manager', or 'Marketing Specialist'.
14. Find vendors with credit ratings of 1, 2, or 3.
15. List all sales orders made by customers with IDs 11000, 12000, and 13000.
<!-- ### 4. **AND Clause** -->
16. Retrieve products that have a `ListPrice` greater than $1000 and are in the 'Components' category.
17. Find customers who live in 'CA' and have a `PersonType` of 'IN'.
18. List employees who are female and have a hire date after January 1, 2010.
19. Retrieve sales orders with a `TotalDue` greater than $5000 and a `ShipDate` within the last 30 days.
20. Find products that have a `StandardCost` between $200 and $500 and a `ListPrice` greater than $1000.
<!-- ### 5. **OR Clause** -->
21. Find customers who live in 'WA' or 'OR'.
22. Retrieve employees who have the job title 'Sales Representative' or 'Sales Manager'.
23. List products that are either in the 'Bikes' category or have a `ListPrice` greater than $2000.
24. Find vendors with a credit rating of 4 or located in the 'Pacific' region.
25. Retrieve sales orders with a `TotalDue` less than $1000 or placed in the year 2019.
<!-- ### 6. **DISTINCT Clause** -->
26. List all distinct job titles of employees.
27. Retrieve all distinct product categories.
28. Find all distinct states where customers are located.
29. List all distinct sales territories.
30. Retrieve all distinct product colors available.
<!-- ### 7. **Combining LIKE with AND/OR** -->
31. Retrieve products whose name starts with 'Touring' and end with 'Bike'.
32. Find customers whose first name starts with 'J' and last name ends with 'son'.
33. List employees whose job title contains 'Engineer' or 'Manager'.
34. Retrieve vendors whose name contains 'Parts' and is located in 'Canada'.
35. Find products whose `ProductNumber` starts with 'BK' and ends with '00'.
<!-- ### 8. **Combining BETWEEN with AND/OR** -->
36. Retrieve sales orders placed between January 1, 2018, and December 31, 2018, and have a `TotalDue` greater than $5000.
37. Find products with a `ListPrice` between $1000 and $2000 or a `StandardCost` between $500 and $1000.
38. List employees hired between January 1, 2010, and January 1, 2015, or whose job title contains 'Manager'.
39. Retrieve purchase orders placed between January 1, 2020, and December 31, 2020, and with a `Freight` cost greater than $100.
40. Find customers with customer IDs between 10000 and 15000 or live in the state of 'FL'.
<!-- ### 9. **Combining IN with AND/OR** -->
41. Retrieve products in the 'Touring-3000', 'Mountain-1000', or 'Road-1500' series and have a `ListPrice` greater than $1000.
42. Find customers who live in 'TX', 'FL', or 'NY' and have a `PersonType` of 'IN'.
43. List employees who have the job titles 'Production Technician', 'Quality Assurance', or 'Maintenance Technician' and were hired after January 1, 2015.
44. Retrieve sales orders made by customers with IDs 11000, 12000, or 13000 and placed within the last 60 days.
45. Find vendors with credit ratings of 2, 3, or 4 and located in 'Europe' or 'Asia'.
 <!-- ### 10. **REGEX_LIKE Clause** -->
46. Find products whose `Name` contains only letters and numbers (no special characters).
47. Retrieve customers whose `EmailAddress` follows the format 'firstname.lastname@domain.com'.
48. List employees whose `PhoneNumber` matches the format '(XXX) XXX-XXXX'.
49. Find vendors whose `AccountNumber` starts with '1' and contains exactly 10 digits.
50. Retrieve products whose `ProductNumber` starts with two letters followed by three digits.

---

