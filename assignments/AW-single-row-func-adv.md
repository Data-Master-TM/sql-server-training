### **Assignment: Advanced SQL Queries Using Single Row Functions on Adventure Works**


##### **Instructions:**
**Execute your queries on the Adventure Works database and analyze the results.**



<br>  
<br>  


### **Questions:**



#### **1.**
Retrieve the `ProductNumber` and `ListPrice` from the `Production.Product` table. Calculate the absolute difference between `ListPrice` and `StandardCost`, round the result to 2 decimal places, and concatenate the `ProductNumber` with the result as a string.

<!-- `ABS()`, `ROUND()`, `CONCAT()`, `CAST()` -->

---

#### **2.**
From the `Sales.SalesOrderHeader` table, retrieve the `OrderDate` and `DueDate`. Calculate the number of days between the two, add 5 days to the `DueDate`, and check if the new `DueDate` is still earlier than today’s date.

<!-- `DATEDIFF()`, `DATEADD()`, `GETDATE()`, `CASE()` -->

---

#### **3.**
Retrieve the `FirstName`, `LastName`, and `EmailAddress` from the `Person.Person` table. Concatenate the `FirstName`, `LastName`, and `EmailAddress`, convert the result to uppercase, and find the length of the final string.

<!-- `CONCAT()`, `UPPER()`, `LEN()` -->

---

#### **4.**
Retrieve the `SalesOrderID` and `OrderDate` from the `Sales.SalesOrderHeader` table. Convert the `OrderDate` to a string format, extract the year and month, and create a new string combining `SalesOrderID`, year, and month.

<!-- `CAST()`, `YEAR()`, `MONTH()`, `CONCAT()` -->

---

#### **5.**
From the `Production.Product` table, retrieve the `ProductNumber` and `StandardCost`. Add 10% to `StandardCost`, round it to 2 decimal places, convert it to a string, and concatenate it with the `ProductNumber`.

<!-- `ROUND()`, `CAST()`, `CONCAT()` -->

---

#### **6.**
Retrieve the `BusinessEntityID` and `ModifiedDate` from the `Person.Person` table. Find how many months have passed since the `ModifiedDate`, and if it’s more than 12 months, append "Outdated" to `BusinessEntityID`; otherwise, append "Current".

<!-- `DATEDIFF()`, `CASE()`, `CONCAT()` -->

---

#### **7.**
Retrieve the `ProductNumber` and `ListPrice` from the `Production.Product` table. Find the position of the first hyphen `'-'` in `ProductNumber`, extract the part of `ProductNumber` before the hyphen, and concatenate it with the `ListPrice` as a string.

<!-- `CHARINDEX()`, `SUBSTRING()`, `CONCAT()`, `CAST()` -->

---

#### **8.**
From the `Sales.SalesOrderHeader` table, retrieve the `OrderDate` and `ShipDate`. Calculate the difference in days, add 3 days to `OrderDate`, and convert both the `OrderDate` and the calculated date to strings for comparison.

<!-- `DATEDIFF()`, `DATEADD()`, `CAST()`, `CONCAT()` -->

---

#### **9.**
Retrieve the `FirstName`, `LastName`, and `Title` from the `Person.Person` table. If `Title` is not null, concatenate it with the `LastName`; otherwise, just display the `LastName` in uppercase.

<!-- `ISNULL()`, `CONCAT()`, `UPPER()` -->

---

#### **10.**
Retrieve the `SalesOrderID`, `OrderDate`, and `TotalDue` from the `Sales.SalesOrderHeader` table. Add 5% to `TotalDue`, convert the result to a string with two decimal places, and concatenate it with the year of the `OrderDate`.

<!-- `ROUND()`, `DATEPART()`, `CAST()`, `CONCAT()` -->

---

#### **11.**
Retrieve the `BusinessEntityID` and `ModifiedDate` from the `Person.Person` table. Convert the `ModifiedDate` to a date-only format, extract the year, and concatenate it with the `BusinessEntityID`.

<!-- `CAST()`, `YEAR()`, `CONCAT()` -->

---

#### **12.**
From the `Production.Product` table, retrieve the `ProductNumber` and `Weight`. If `Weight` is null, display "Weight Unavailable"; otherwise, convert the `Weight` to a string and append " kg" to it.

<!-- `ISNULL()`, `CONCAT()`, `CAST()` -->

---

#### **13.**
Retrieve the `OrderDate`, `ShipDate`, and `TotalDue` from the `Sales.SalesOrderHeader` table. Calculate the number of months between `OrderDate` and `ShipDate`, convert the `TotalDue` to an integer, and concatenate it with the calculated months.

<!-- `DATEDIFF()`, `CAST()`, `CONCAT()` -->

---

#### **14.**
Retrieve the `FirstName`, `LastName`, and `BirthDate` from the `Person.Person` table. Convert `BirthDate` to a string format, find the first 3 characters of `FirstName`, and concatenate them with the `LastName` and the year of `BirthDate`.

<!-- `SUBSTRING()`, `YEAR()`, `CONCAT()`, `CAST()` -->

---

#### **15.**
Retrieve the `ProductNumber` from the `Production.Product` table. Extract the last 3 characters of `ProductNumber`, find its length, and concatenate it with the original `ProductNumber` reversed.

<!-- `RIGHT()`, `LEN()`, `CONCAT()`, `REVERSE()` -->

---

#### **16.**
Retrieve the `SalesOrderID` and `OrderDate` from the `Sales.SalesOrderHeader` table. Subtract 7 days from `OrderDate`, convert the result to a string, and append it to the `SalesOrderID`.

<!-- `DATEADD()`, `CAST()`, `CONCAT()` -->

---

#### **17.**
From the `Production.Product` table, retrieve the `ProductNumber` and `StandardCost`. If the `StandardCost` is below 50, multiply it by 2, round the result, and concatenate it with `ProductNumber`.

<!-- `CASE()`, `ROUND()`, `CONCAT()`, `CAST()` -->

---

#### **18.**
Retrieve the `SalesOrderID` and `TotalDue` from the `Sales.SalesOrderHeader` table. Calculate the percentage of `TotalDue` relative to the highest `TotalDue`, round it to 2 decimal places, and append it to `SalesOrderID`.

<!-- `MAX()`, `CAST()`, `CONCAT()`, `ROUND()` -->

---

#### **19.**
Retrieve the `ProductNumber` and `ListPrice` from the `Production.Product` table. Subtract 5% from the `ListPrice`, convert the result to money data type, and concatenate it with `ProductNumber`.

<!-- `ROUND()`, `CAST()`, `CONCAT()` -->

---

#### **20.**
Retrieve the `FirstName`, `MiddleName`, and `LastName` from the `Person.Person` table. If `MiddleName` is null, display the initials of `FirstName` and `LastName`; otherwise, display the initials of `FirstName`, `MiddleName`, and `LastName`.

<!-- `ISNULL()`, `SUBSTRING()`, `CONCAT()` -->

---

#### **21.**
Retrieve the `SalesOrderID`, `OrderDate`, and `ShipDate` from the `Sales.SalesOrderHeader` table. Calculate the total number of days from `OrderDate` to `ShipDate`, and concatenate the result with the `SalesOrderID`.

<!-- `DATEDIFF()`, `CONCAT()`, `CAST()` -->

---

#### **22.**
From the `Production.Product` table, retrieve the `ProductNumber` and `ListPrice`. Increase the `ListPrice` by 20%, round it to 2 decimal places, and append the rounded value to the `ProductNumber`.

<!-- `ROUND()`, `CONCAT()`, `CAST()` -->

---

#### **23.**
Retrieve the `BusinessEntityID` and `ModifiedDate` from the `Person.Person` table. Add 30 days to the `ModifiedDate`, convert it to a string format, and concatenate it with the `BusinessEntityID`.

<!-- `DATEADD()`, `CAST()`, `CONCAT()` -->

---

#### **24.**
From the `Production.Product` table, retrieve the `ProductNumber` and `Weight`. If `Weight` is null, set it to 1, multiply it by 2, and convert it to a string format for display.

<!-- `ISNULL()`, `CAST()`, `CONCAT()` -->

---

#### **25.**
Retrieve the `SalesOrderID`, `OrderDate`, and `TotalDue` from the `Sales.SalesOrderHeader` table. Convert `OrderDate` to a string format, and concatenate it with the rounded `TotalDue`.

<!-- `CAST()`, `ROUND()`, `CONCAT()` -->

---

#### **26.**
Retrieve the `ProductNumber` and `Name`

 from the `Production.Product` table. Reverse the `ProductNumber`, find its length, and concatenate it with the `Name`.

<!-- `REVERSE()`, `LEN()`, `CONCAT()` -->

---

#### **27.**
From the `Sales.SalesOrderHeader` table, retrieve the `OrderDate` and `ShipDate`. Calculate the difference in days, add 3 days to the `ShipDate`, and convert the `ShipDate` to a string.

<!-- `DATEDIFF()`, `DATEADD()`, `CAST()` -->

---

#### **28.**
Retrieve the `FirstName`, `LastName`, and `EmailPromotion` from the `Person.Person` table. If `EmailPromotion` is 1, display "Yes"; otherwise, display "No" along with the `LastName`.

<!-- `CASE()`, `CONCAT()`, `CAST()` -->

---

#### **29.**
Retrieve the `ProductNumber` and `ListPrice` from the `Production.Product` table. If `ListPrice` is greater than 100, subtract 10 from it and convert it to a string, then concatenate with `ProductNumber`.

<!-- `CASE()`, `CONCAT()`, `CAST()` -->

---

#### **30.**
Retrieve the `SalesOrderID` and `TotalDue` from the `Sales.SalesOrderHeader` table. Calculate the absolute difference between `TotalDue` and `Freight`, round the result, and append it to `SalesOrderID`.

<!-- `ABS()`, `ROUND()`, `CONCAT()`, `CAST()` -->

---

#### **31.**
Retrieve the `ProductNumber` and `StandardCost` from the `Production.Product` table. Multiply `StandardCost` by 1.1, round it to 2 decimal places, and convert it to money format, then concatenate with `ProductNumber`.

<!-- `ROUND()`, `CAST()`, `CONCAT()` -->

---

#### **32.**
Retrieve the `OrderDate` and `ShipDate` from the `Sales.SalesOrderHeader` table. Calculate the number of days between them, and display it along with the first 5 characters of `SalesOrderID`.

<!-- `DATEDIFF()`, `SUBSTRING()`, `CONCAT()` -->

---

#### **33.**
Retrieve the `FirstName`, `LastName`, and `Title` from the `Person.Person` table. If `Title` is null, convert `LastName` to uppercase and display; otherwise, display the original `LastName`.

<!-- `ISNULL()`, `UPPER()`, `CONCAT()` -->

---

#### **34.**
From the `Production.Product` table, retrieve the `ProductNumber` and `ListPrice`. Calculate the square root of `ListPrice`, round it to 2 decimal places, and convert to string format for display.

<!-- `SQRT()`, `ROUND()`, `CAST()`, `CONCAT()` -->

---

#### **35.**
Retrieve the `SalesOrderID` and `OrderDate` from the `Sales.SalesOrderHeader` table. Subtract 15 days from `OrderDate`, convert it to a string, and append to the first 4 characters of `SalesOrderID`.

<!-- `DATEADD()`, `SUBSTRING()`, `CAST()`, `CONCAT()` -->

---

#### **36.**
Retrieve the `ProductNumber` and `StandardCost` from the `Production.Product` table. If `StandardCost` is above 100, divide it by 2, round to 2 decimal places, and concatenate with `ProductNumber`.

<!-- `CASE()`, `ROUND()`, `CONCAT()`, `CAST()` -->

---

#### **37.**
Retrieve the `SalesOrderID` and `TotalDue` from the `Sales.SalesOrderHeader` table. Calculate the ceiling value of `TotalDue`, convert it to a string, and concatenate with the `SalesOrderID`.

<!-- `CEILING()`, `CAST()`, `CONCAT()` -->

---

#### **38.**
From the `Production.Product` table, retrieve the `ProductNumber` and `StandardCost`. If `StandardCost` is null, display "N/A"; otherwise, convert it to money format and concatenate with `ProductNumber`.

<!-- `ISNULL()`, `CAST()`, `CONCAT()` -->

---

#### **39.**
Retrieve the `OrderDate` and `ShipDate` from the `Sales.SalesOrderHeader` table. Calculate the number of months between them, and concatenate it with the year part of `OrderDate`.

<!-- `DATEDIFF()`, `YEAR()`, `CONCAT()`, `CAST()` -->

---

#### **40.**
Retrieve the `FirstName`, `LastName`, and `MiddleName` from the `Person.Person` table. If `MiddleName` is not null, concatenate the first character of `FirstName`, `MiddleName`, and `LastName` as initials.

<!-- `ISNULL()`, `SUBSTRING()`, `CONCAT()` -->

---

#### **41.**
Retrieve the `ProductNumber` and `Name` from the `Production.Product` table. Convert the first 3 characters of `ProductNumber` to uppercase, find its position in the `Name`, and concatenate both for display.

<!-- `UPPER()`, `CHARINDEX()`, `CONCAT()` -->

---

#### **42.**
Retrieve the `SalesOrderID`, `OrderDate`, and `ShipDate` from the `Sales.SalesOrderHeader` table. If `OrderDate` is greater than `ShipDate`, subtract 10 days from `ShipDate` and convert it to a string.

<!-- `CASE()`, `DATEADD()`, `CAST()`, `CONCAT()` -->

---

#### **43.**
From the `Production.Product` table, retrieve the `ProductNumber` and `ListPrice`. Convert `ListPrice` to an integer, and append it to the first 5 characters of `ProductNumber`.

<!-- `CAST()`, `SUBSTRING()`, `CONCAT()` -->

---

#### **44.**
Retrieve the `SalesOrderID` and `TotalDue` from the `Sales.SalesOrderHeader` table. Multiply `TotalDue` by 1.15, round to 2 decimal places, and convert it to money format, then concatenate with `SalesOrderID`.

<!-- `ROUND()`, `CAST()`, `CONCAT()` -->

---

#### **45.**
Retrieve the `OrderDate` and `DueDate` from the `Sales.SalesOrderHeader` table. Calculate the difference in days, subtract 5 days from `DueDate`, and convert to string format.

<!-- `DATEDIFF()`, `DATEADD()`, `CAST()`, `CONCAT()` -->

---

#### **46.**
Retrieve the `ProductNumber` and `StandardCost` from the `Production.Product` table. Convert `StandardCost` to the next highest integer, and concatenate with the first 4 characters of `ProductNumber`.

<!-- `CEILING()`, `SUBSTRING()`, `CONCAT()` -->

---

#### **47.**
From the `Person.Person` table, retrieve the `FirstName`, `LastName`, and `EmailPromotion`. If `EmailPromotion` is 2, display "Active" with the `LastName`; otherwise, display "Inactive".

<!-- `CASE()`, `CONCAT()` -->

---

#### **48.**
Retrieve the `SalesOrderID` and `OrderDate` from the `Sales.SalesOrderHeader` table. Convert the `OrderDate` to a date format, add 10 days to it, and concatenate it with the first 3 characters of `SalesOrderID`.

<!-- `CAST()`, `DATEADD()`, `CONCAT()`, `SUBSTRING()` -->

---

#### **49.**
Retrieve the `ProductNumber` and `Name` from the `Production.Product` table. Reverse the `ProductNumber`, and concatenate it with the length of `Name`.

<!-- `REVERSE()`, `LEN()`, `CONCAT()` -->

---

#### **50.**
Retrieve the `OrderDate`, `ShipDate`, and `TotalDue` from the `Sales.SalesOrderHeader` table. Calculate the absolute difference between `TotalDue` and `Freight`, round to 2 decimal places, and concatenate it with the month part of `OrderDate`.

<!-- `ABS()`, `ROUND()`, `MONTH()`, `CONCAT()` -->
