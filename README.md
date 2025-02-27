# Customer Data Analysis Queries

## Table Creation

```sql
CREATE TABLE Customers (
    CustomerID VARCHAR(20) PRIMARY KEY,
    Profession VARCHAR(100),
    Age VARCHAR(5),
    Gender VARCHAR(10),
    AnnualIncome VARCHAR(20),
    SpendingScore VARCHAR(10),
    WorkExperience VARCHAR(10),
    FamilySize VARCHAR(10)
);

-- Viewing the first 10 records
SELECT TOP 10 * FROM Customers;

-- Altering column data types for better query performance
ALTER TABLE Customers  
ALTER COLUMN Age INT;  

ALTER TABLE Customers  
ALTER COLUMN AnnualIncome DECIMAL(10,2);  

ALTER TABLE Customers  
ALTER COLUMN SpendingScore INT;  

ALTER TABLE Customers  
ALTER COLUMN WorkExperience INT;  

ALTER TABLE Customers  
ALTER COLUMN FamilySize INT;
