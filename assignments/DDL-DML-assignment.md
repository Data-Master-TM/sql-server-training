## SQL Server Assignment: Data Types, Constraints, DDL, and DML


<br>  

<br>  




## Questions


<!-- ### 1. **Data Types** -->

1. **Create a table named `Employees` with the following columns and appropriate data types:**
    - `EmployeeID` (Primary Key, Integer)
    - `FirstName` (Variable character with a max length of 50)
    - `LastName` (Variable character with a max length of 50)
    - `BirthDate` (Date)
    - `Salary` (Decimal with 18 digits total and 2 decimal places)

2. **What data type would you use to store a large block of text such as a blog post? Create a table `BlogPosts` with a `Content` column for this purpose.**

3. **Create a table named `Products` with the following columns and appropriate data types:**
    - `ProductID` (Primary Key, Integer)
    - `ProductName` (Variable character with a max length of 100)
    - `Price` (Decimal with 10 digits total and 2 decimal places)
    - `StockQuantity` (Integer)

4. **Create a table named `Orders` with an `OrderID` column as the primary key, which should be auto-incremented. What data type should you use?**

5. **How would you define a column in a table to store a fixed-length character string, such as a two-letter country code? Provide an example by creating a `Countries` table with a `CountryCode` column.**

6. **Create a table named `Customers` with the following columns and appropriate data types:**
    - `CustomerID` (Primary Key, Integer)
    - `FullName` (Variable character with a max length of 100)
    - `EmailAddress` (Variable character with a max length of 100)
    - `PhoneNumber` (Variable character with a max length of 15)

7. **What data type would you use to store a timestamp for recording the exact time an event occurred? Create a table named `EventLogs` with a `Timestamp` column for this purpose.**

8. **Create a table named `Inventory` with the following columns:**
    - `InventoryID` (Primary Key, Integer)
    - `ProductID` (Integer, Foreign Key referencing `Products`)
    - `QuantityInStock` (Integer)

9. **Create a `Payments` table with a `PaymentAmount` column that can store values up to $999,999.99 with exactly 2 decimal places. What data type should you use?**

10. **Create a `Users` table with a `Username` column that should not exceed 20 characters. What data type is appropriate?**

<!-- ### 2. **Constraints** -->

11. **Create a table `Departments` with the following constraints:**
    - `DepartmentID` as the primary key
    - `DepartmentName` with a unique constraint

12. **Create a `Products` table with a check constraint on the `Price` column ensuring that it cannot be less than zero.**

13. **Create a `Salaries` table where the `Amount` column must be greater than 0 and cannot exceed $100,000.**

14. **Create a table `Enrollments` with the following columns and constraints:**
    - `EnrollmentID` as the primary key
    - `StudentID` as a foreign key referencing a `Students` table
    - `CourseID` as a foreign key referencing a `Courses` table
    - Ensure that a student can only enroll in the same course once (composite unique constraint on `StudentID` and `CourseID`).

15. **Create a `Vehicles` table with a `VIN` (Vehicle Identification Number) that is exactly 17 characters long.**

16. **Create a `Loans` table where the `LoanAmount` must be between $1,000 and $100,000 (inclusive).**

17. **Create a `Sales` table where the `SaleDate` column cannot be a future date.**

18. **Create a table `Inventory` with a default value of 0 for the `QuantityInStock` column.**

19. **Create a `BankAccounts` table where the `Balance` column cannot be negative.**

20. **Create a `JobApplications` table where the `ApplicationDate` cannot be null.**

<!-- ### 3. **DDL Operations** -->

21. **Write a SQL statement to create a database named `SalesDB`.**

22. **Create a table `Invoices` in the `SalesDB` database with the following columns:**
    - `InvoiceID` (Primary Key, Integer)
    - `CustomerID` (Foreign Key, Integer)
    - `InvoiceDate` (Date)
    - `TotalAmount` (Decimal with 10 digits total and 2 decimal places)

23. **Create an index on the `LastName` column of the `Employees` table.**

24. **Alter the `Products` table to add a new column `Category` (Variable character with a max length of 50).**

25. **Drop the `Orders` table from the database.**

26. **Rename the `Customers` table to `Clientele`.**

27. **Add a new column `MiddleName` (Variable character with a max length of 50) to the `Employees` table, and ensure it can accept null values.**

28. **Alter the `Orders` table to make the `OrderDate` column mandatory (not null).**

29. **Create a unique constraint on the `EmailAddress` column in the `Customers` table.**

30. **Drop the index on the `LastName` column of the `Employees` table.**

<!-- ### 4. **DML Operations** -->

31. **Insert a new record into the `Employees` table with the following details:**
    - `EmployeeID`: 101
    - `FirstName`: 'John'
    - `LastName`: 'Doe'
    - `BirthDate`: '1985-05-15'
    - `Salary`: 60000

32. **Update the `Salary` of the employee with `EmployeeID` 101 to $65,000.**

33. **Delete the employee record from the `Employees` table where `EmployeeID` is 101.**

34. **Insert multiple records into the `Products` table with the following details:**
    - `ProductID`: 201, `ProductName`: 'Mountain Bike', `Price`: 1200.00, `StockQuantity`: 50
    - `ProductID`: 202, `ProductName`: 'Road Bike', `Price`: 1500.00, `StockQuantity`: 30

35. **Update the `Price` of all products in the `Products` table by increasing it by 10%.**

36. **Delete all products from the `Products` table where `StockQuantity` is 0.**

37. **Insert a new order into the `Orders` table with the following details:**
    - `OrderID`: 301
    - `CustomerID`: 401
    - `OrderDate`: '2024-08-29'

38. **Update the `OrderDate` of the order with `OrderID` 301 to '2024-09-01'.**

39. **Delete the order from the `Orders` table where `OrderID` is 301.**

40. **Insert a new customer into the `Customers` table with the following details:**
    - `CustomerID`: 501
    - `FullName`: 'Alice Smith'
    - `EmailAddress`: 'alice.smith@example.com'
    - `PhoneNumber`: '123-456-7890'

<!-- ### 5. **Advanced DDL/DML Operations** 

41. **Create a table `Suppliers` with a foreign key constraint referencing the `Vendors` table.**

42. **Insert data into the `Orders` table and simultaneously insert related records into the `OrderDetails` table using a transaction.**

43. **Alter the `Employees` table to drop the `MiddleName` column.**

44. **Create a view `ActiveProducts` that lists all products from the `Products` table where `StockQuantity` is greater than 0.**

45. **Create a stored procedure `spGetEmployeeByID` that takes an `EmployeeID` as a parameter and returns the corresponding employee's details.**

46. **Create a trigger that automatically updates the `LastUpdated` column of a `Products` table whenever a product’s details are modified.**

47. **Write a query to transfer all products from the `OldProducts` table to the `Products` table and delete them from `OldProducts` afterwards.**

48. **Create a function `fnCalculateDiscount` that calculates a discount on a product based on its price.**

49. **Use a CTE (Common Table Expression) to retrieve all employees who earn more than $50,000.**

50. **Create a sequence named `OrderNumberSeq` that starts from 1000 and increments by 1. Use this sequence to generate order numbers in the `Orders` table.**

-->

---

