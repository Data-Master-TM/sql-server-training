### Step 1: Create the Database

```sql
CREATE DATABASE EcommerceDB;
GO

USE EcommerceDB;
GO
```

### Step 2: Create Tables with Relationships

```sql
CREATE TABLE Customers (
    CustomerID int PRIMARY KEY IDENTITY(1,1),
    FirstName varchar(50) NOT NULL,
    LastName varchar(50) NOT NULL,
    Email varchar(100) UNIQUE NOT NULL,
    Phone varchar(50),
    Address varchar(255),
    City varchar(50),
    Country varchar(50)
);

CREATE TABLE Categories (
    CategoryID int PRIMARY KEY IDENTITY(1,1),
    CategoryName varchar(100) NOT NULL
);

CREATE TABLE Products (
    ProductID int PRIMARY KEY IDENTITY(1,1),
    ProductName varchar(100) NOT NULL,
    CategoryID int FOREIGN KEY REFERENCES Categories(CategoryID),
    Price decimal(10, 2) NOT NULL,
    StockQuantity int NOT NULL DEFAULT 0
);

CREATE TABLE Orders (
    OrderID int PRIMARY KEY IDENTITY(1,1),
    CustomerID int FOREIGN KEY REFERENCES Customers(CustomerID),
    OrderDate datetime DEFAULT GETDATE(),
    TotalAmount decimal(10, 2) NOT NULL
);

CREATE TABLE OrderDetails (
    OrderDetailID int PRIMARY KEY IDENTITY(1,1),
    OrderID int FOREIGN KEY REFERENCES Orders(OrderID),
    ProductID int FOREIGN KEY REFERENCES Products(ProductID),
    Quantity int NOT NULL,
    UnitPrice decimal(10, 2) NOT NULL,
    TotalPrice AS (Quantity * UnitPrice) PERSISTED
);
```

### Step 3: Insert Sample Data into Categories and Products

```sql
INSERT INTO Categories (CategoryName)
VALUES 
('Electronics'),
('Books'),
('Clothing');

INSERT INTO Products (ProductName, CategoryID, Price, StockQuantity)
VALUES 
('Laptop', 1, 999.99, 50),
('Smartphone', 1, 699.99, 100),
('T-shirt', 3, 19.99, 200),
('Novel', 2, 14.99, 150);
```

### Step 4: Insert 1,000 Customers

We will use a loop to insert 1,000 customers with varied names, emails, and other details.

```sql
DECLARE @Counter int = 1;

WHILE @Counter <= 1000
BEGIN
    INSERT INTO Customers (FirstName, LastName, Email, Phone, Address, City, Country)
    VALUES 
    (
        CONCAT('First', @Counter), 
        CONCAT('Last', @Counter), 
        CONCAT('email', @Counter, '@example.com'), 
        CONCAT('12345678', RIGHT('0000' + CAST(@Counter AS varchar(4)), 4)), 
        CONCAT('Address ', @Counter), 
        CONCAT('City ', @Counter), 
        'USA'
    );

    SET @Counter = @Counter + 1;
END
```

### Step 5: Insert Sample Orders and OrderDetails

We'll create orders and order details for each customer. To ensure diversity, we'll randomly assign products to orders.

```sql
-- Insert Orders
DECLARE @OrderCounter int = 1;

WHILE @OrderCounter <= 1000
BEGIN
    INSERT INTO Orders (CustomerID, TotalAmount)
    VALUES 
    (
        @OrderCounter,
        -- Simulate a random total amount between 50 and 500
        CAST(RAND() * 450 + 50 AS decimal(10, 2))
    );

    SET @OrderCounter = @OrderCounter + 1;
END

-- Insert OrderDetails
DECLARE @DetailCounter int = 1;

WHILE @DetailCounter <= 1000
BEGIN
    INSERT INTO OrderDetails (OrderID, ProductID, Quantity, UnitPrice)
    VALUES 
    (
        -- Randomly assign an existing order
        CAST(RAND() * 999 + 1 AS int),
        -- Randomly assign an existing product
        CAST(RAND() * 4 + 1 AS int),
        -- Randomly assign quantity between 1 and 5
        CAST(RAND() * 4 + 1 AS int),
        -- Use product price for unit price
        (SELECT Price FROM Products WHERE ProductID = CAST(RAND() * 4 + 1 AS int))
    );

    SET @DetailCounter = @DetailCounter + 1;
END
```

### Summary of the Data

- **1,000 Customers** with unique names, emails, and addresses.
- **4 Categories** for Products.
- **4 Products** assigned to the categories.
- **1,000 Orders** placed by customers.
- **1,000 Order Details** linked to orders and products.

### Example Queries

To verify and practice with the data, you can use the following queries:

#### Retrieve all Orders with Customer Details

```sql
SELECT 
    O.OrderID,
    C.FirstName + ' ' + C.LastName AS CustomerName,
    O.OrderDate,
    O.TotalAmount
FROM Orders O
JOIN Customers C ON O.CustomerID = C.CustomerID;
```

#### Retrieve Order Details for a Specific Order

```sql
SELECT 
    OD.OrderDetailID,
    P.ProductName,
    OD.Quantity,
    OD.UnitPrice,
    OD.TotalPrice
FROM OrderDetails OD
JOIN Products P ON OD.ProductID = P.ProductID
WHERE OD.OrderID = 1;
```

#### Check Available Stock for Products

```sql
SELECT 
    ProductName,
    StockQuantity
FROM Products
WHERE StockQuantity > 0;
```

#### List Products by Category

```sql
SELECT 
    C.CategoryName,
    P.ProductName,
    P.Price
FROM Products P
JOIN Categories C ON P.CategoryID = C.CategoryID;
```
