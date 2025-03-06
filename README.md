ques 1) 

CREATE TABLE Employees (
    EmployeeID INT PRIMARY KEY,
    FirstName VARCHAR(50),
    LastName VARCHAR(50),
    DateOfBirth DATE,
    Salary DECIMAL(10,2)
);

ques 2) 

SELECT ProductName, Price 
FROM Products 
WHERE Price > 100 AND Price < 1000;

ques 3) 

SELECT TABLE_NAME 
FROM INFORMATION_SCHEMA.TABLES 
WHERE TABLE_TYPE = 'BASE TABLE';

ques 4) 

CREATE TABLE Orders (
    OrderID INT PRIMARY KEY,
    OrderDate DATETIME,
    CustomerName VARCHAR(100),
    TotalAmount DECIMAL(10,2),
    Shipped BIT
);

ques 5 ) SELECT * FROM Customers;

Ques 6 ) SELECT DISTINCT City 
FROM Customers 
ORDER BY City ASC;

ques 7) 
CREATE TABLE Sales (
    SalesID INT PRIMARY KEY,
    SalesPersonID INT,
    SalesAmount DECIMAL(10,2)
);

INSERT INTO Sales (SalesID, SalesPersonID, SalesAmount) VALUES 
(1, 101, 6000),
(2, 102, 4500),
(3, 101, 7000),
(4, 103, 8000),
(5, 102, 5200);

SELECT SalesPersonID, SUM(SalesAmount) AS TotalSales 
FROM Sales 
WHERE SalesAmount > 5000 
GROUP BY SalesPersonID; 

ques 13)

SELECT * FROM Employees WHERE Salary > 50000;

ques 14)

SELECT 
    SUM(Salary) AS TotalSalary,
    AVG(Salary) AS AverageSalary,
    MAX(Salary) AS MaxSalary,
    MIN(Salary) AS MinSalary
FROM Employees;

ques 15)

CREATE TABLE Departments (
    DepartmentID INT PRIMARY KEY,
    DepartmentName NVARCHAR(100) NOT NULL
);

INSERT INTO Departments (DepartmentID, DepartmentName) VALUES
(1, 'HR'),
(2, 'IT'),
(3, 'Finance');

ques 16) 
SELECT E.FirstName, E.LastName, D.DepartmentName 
FROM Employees E
JOIN Departments D ON E.DepartmentID = D.DepartmentID;
