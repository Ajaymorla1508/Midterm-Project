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
```

---

## Altering Column Data Types

```sql
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
```

---

## Queries for Data Analysis

### 1. Sum of Annual Income by Profession

```sql
SELECT Profession, SUM(AnnualIncome) AS TotalAnnualIncome
FROM Customers
GROUP BY Profession
ORDER BY TotalAnnualIncome DESC;
```

### 2. Sum of Spending Score by Gender

```sql
SELECT Gender, SUM(SpendingScore) AS TotalSpendingScore
FROM Customers
GROUP BY Gender
ORDER BY TotalSpendingScore DESC;
```

### 3. Sum of Spending Score by Profession

```sql
SELECT Profession, SUM(SpendingScore) AS TotalSpendingScore
FROM Customers
GROUP BY Profession
ORDER BY TotalSpendingScore DESC;
```

### 4. Count of CustomerID by Gender (Pie Chart)

```sql
SELECT Gender, COUNT(CustomerID) AS CustomerCount
FROM Customers
GROUP BY Gender;
```

### 5. Sum of Spending Score by Family Size

```sql
SELECT FamilySize, SUM(SpendingScore) AS TotalSpendingScore
FROM Customers
GROUP BY FamilySize
ORDER BY FamilySize;
```

### 6. Sum of Annual Income by Work Experience

```sql
SELECT WorkExperience, SUM(AnnualIncome) AS TotalAnnualIncome
FROM Customers
GROUP BY WorkExperience
ORDER BY WorkExperience;
```

### 7. Sum of Spending Score by Gender (Donut Chart)

```sql
SELECT Gender, SUM(SpendingScore) AS TotalSpendingScore
FROM Customers
GROUP BY Gender
ORDER BY TotalSpendingScore DESC;
```

