### **Assignment: Comprehensive SQL Server Functions Exploration Using Adventure Works**

#### **Instructions:**
 **Execute your queries on the Adventure Works database and analyze the results.**


---

<!--  ### **Character Functions** -->

1. **Q1:** Retrieve the `FirstName` and `LastName` from the `Person.Person` table. Display `FirstName` in uppercase using the **`UPPER()`** function.
2. **Q2:** Convert the `LastName` to lowercase using the **`LOWER()`** function.
3. **Q3:** Concatenate `FirstName` and `LastName` with a comma and space in between using the **`CONCAT()`** function.
4. **Q4:** Extract the first 5 characters of `LastName` using the **`LEFT()`** function.
5. **Q5:** Extract the last 4 characters of `EmailAddress` from the `Person.EmailAddress` table using the **`RIGHT()`** function.
6. **Q6:** Calculate the length of `EmailAddress` using the **`LEN()`** function.
7. **Q7:** Reverse the `FirstName` using the **`REVERSE()`** function.
8. **Q8:** Find the position of the '@' symbol in `EmailAddress` using the **`CHARINDEX()`** function.
9. **Q9:** Trim leading spaces from `MiddleName` in the `Person.Person` table using the **`LTRIM()`** function.
10. **Q10:** Trim trailing spaces from `Title` in the `Person.Person` table using the **`RTRIM()`** function.
11. **Q11:** Trim both leading and trailing spaces from `Title` using the **`TRIM()`** function.
12. **Q12:** Replace all occurrences of 'e' in `FirstName` with 'E' using the **`REPLACE()`** function.
13. **Q13:** Translate 'abc' in `FirstName` to 'xyz' using the **`TRANSLATE()`** function.
14. **Q14:** Use **`SUBSTRING()`** to extract the middle 3 characters of `LastName` starting from the 3rd character.
15. **Q15:** Combine **`LEN()`** and **`LEFT()`** to display the first half of the `LastName`.

---

<!--  ### **Numeric Functions** -->

16. **Q16:** Retrieve the `ListPrice` from the `Production.Product` table and round it to the nearest whole number using the **`ROUND()`** function.
17. **Q17:** Round the `StandardCost` to 1 decimal place using the **`ROUND()`** function.
18. **Q18:** Calculate the square root of `StandardCost` using the **`SQRT()`** function.
19. **Q19:** Find the absolute value of the difference between `ListPrice` and `StandardCost` using the **`ABS()`** function.
20. **Q20:** Raise `Weight` to the power of 2 using the **`POWER()`** function.
21. **Q21:** Calculate the floor value of `Weight` using the **`FLOOR()`** function.
22. **Q22:** Calculate the ceiling value of `Weight` using the **`CEILING()`** function.
23. **Q23:** Use **`POWER()`** to calculate `ListPrice` raised to the power of 3.
24. **Q24:** Use **`ROUND()`** to round the square root of `StandardCost` to 2 decimal places.
25. **Q25:** Calculate the absolute value of `ProductSubcategoryID` subtracted from `ProductCategoryID` using the **`ABS()`** function.

---

<!--  ### **Date Functions** -->

26. **Q26:** Retrieve the current system date and time using the **`GETDATE()`** function.
27. **Q27:** Retrieve the current system date and time using the **`CURRENT_TIMESTAMP`** function.
28. **Q28:** Extract the year from `OrderDate` in the `Sales.SalesOrderHeader` table using the **`YEAR()`** function.
29. **Q29:** Extract the month from `OrderDate` using the **`MONTH()`** function.
30. **Q30:** Extract the day from `OrderDate` using the **`DAY()`** function.
31. **Q31:** Use **`DATEDIFF()`** to calculate the number of days between `OrderDate` and `ShipDate`.
32. **Q32:** Add 1 year to `OrderDate` using the **`DATEADD()`** function.
33. **Q33:** Add 15 days to `OrderDate` using the **`DATEADD()`** function.
34. **Q34:** Check if the value '2024-08-31' is a valid date using the **`ISDATE()`** function.
35. **Q35:** Use **`EOMONTH()`** to find the last day of the month for each `OrderDate`.
36. **Q36:** Find the first day of the current year by using **`DATETRUNC()`** on the current date.
37. **Q37:** Calculate the number of months between `OrderDate` and `ShipDate` using **`DATEDIFF()`**.
38. **Q38:** Subtract 5 hours from `OrderDate` using the **`DATEADD()`** function.
39. **Q39:** Use **`GETDATE()`** and **`DATEADD()`** to find the date 100 days from today.
40. **Q40:** Use **`ISDATE()`** to check if `ShipDate` is a valid date.

---

<!--  ### **Data Type Conversion Functions** -->

41. **Q41:** Convert `OrderDate` from the `Sales.SalesOrderHeader` table to a varchar format using the **`CAST()`** function.
42. **Q42:** Convert `TotalDue` from `Sales.SalesOrderHeader` to an integer using the **`CONVERT()`** function.
43. **Q43:** Convert `ProductNumber` from `Production.Product` to binary data using the **`CAST()`** function.
44. **Q44:** Use **`ISNULL()`** to replace `NULL` values in `CreditCardApprovalCode` with 'Not Available'.
45. **Q45:** Convert `ModifiedDate` to a date-only format using **`CONVERT()`** with the appropriate style.
46. **Q46:** Use **`CAST()`** to convert `SalesOrderID` to a char(10) and concatenate with a string.
47. **Q47:** Convert the `DueDate` to a different datetime format using **`CONVERT()`** and style code.
48. **Q48:** Replace `NULL` values in `Freight` with 0 using **`ISNULL()`**.
49. **Q49:** Convert `TotalDue` to money data type using **`CAST()`**.
50. **Q50:** Use **`CAST()`** to convert `StandardCost` to a decimal with 4 decimal places.

---
