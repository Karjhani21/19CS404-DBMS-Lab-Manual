**Question 1**
--
-- Insert a product with ProductID 104, Name Tablet, and Category Electronics into the Products table, where Price and Stock should use default values.

```sql
-- INSERT INTO Products (ProductID, Name, Category)  
VALUES (104, 'Tablet', 'Electronics');
```

**Output:**

![image](https://github.com/user-attachments/assets/955b9f60-0f0f-4ca4-b524-d6c4160b9939)


**Question 2**
---
--Create a table named Bonuses with the following constraints:
BonusID as INTEGER should be the primary key.
EmployeeID as INTEGER should be a foreign key referencing Employees(EmployeeID).
BonusAmount as REAL should be greater than 0.
BonusDate as DATE.
Reason as TEXT should not be NULL.

```sql
-- create table Bonuses(
BonusID integer primary key,
EmployeeID integer,
BonusAmount real check(BonusAmount>0),
BonusDate date,
Reason text not null,
foreign key (EmployeeID)references Employees(EmployeeID)
);
```

**Output:**
![image](https://github.com/user-attachments/assets/39f45e15-1101-423e-8b55-f3cb5695011b)


**Question 3**
---
-- Create a table named Shipments with the following constraints:
ShipmentID as INTEGER should be the primary key.
ShipmentDate as DATE.
SupplierID as INTEGER should be a foreign key referencing Suppliers(SupplierID).
OrderID as INTEGER should be a foreign key referencing Orders(OrderID).

```sql
-- CREATE TABLE Shipments (
    ShipmentID INTEGER PRIMARY KEY,
    ShipmentDate DATE,
    SupplierID INTEGER,
    OrderID INTEGER,
    FOREIGN KEY (SupplierID) REFERENCES Suppliers(SupplierID),
    FOREIGN KEY (OrderID) REFERENCES Orders(OrderID)
);
```

**Output:**

![image](https://github.com/user-attachments/assets/9e143b0f-2957-4ada-b103-5df7d5ce3f79)


**Question 4**
---
-- Create a table named ProjectAssignments with the following constraints:
AssignmentID as INTEGER should be the primary key.
EmployeeID as INTEGER should be a foreign key referencing Employees(EmployeeID).
ProjectID as INTEGER should be a foreign key referencing Projects(ProjectID).
AssignmentDate as DATE should be NOT NULL.

```sql
-- CREATE TABLE ProjectAssignments (
AssignmentID INTEGER PRIMARY KEY,
EmployeeID INTEGER,
ProjectID INTEGER,
AssignmentDate DATE NOT NULL,
FOREIGN KEY (EmployeeID) REFERENCES  Employees(EmployeeID),
FOREIGN KEY (ProjectID) REFERENCES Projects(ProjectID)
);
```

**Output:**

![image](https://github.com/user-attachments/assets/8d9fd97c-a427-4fa2-b890-5693fafb670c)


**Question 5**
---
-- Create a table named Department with the following constraints:
DepartmentID as INTEGER should be the primary key.
DepartmentName as TEXT should be unique and not NULL.
Location as TEXT.

```sql
-- CREATE TABLE Department(
DepartmentID INTEGER PRIMARY KEY,
DepartmentName TEXT UNIQUE NOT NULL,
Location TEXT
);
```

**Output:**

![image](https://github.com/user-attachments/assets/a51d42a5-734d-4334-af90-d13fe3c80602)


**Question 6**
---
-- Write a SQL Query  to Rename attribute "name" to "first_name"  and add mobilenumber as number ,DOB as Date,State as varchar(30) in the table Companies. 

```sql
-- ALTER TABLE Companies RENAME COLUMN name TO first_name;
ALTER TABLE Companies ADD COLUMN mobilenumber number;
ALTER TABLE Companies ADD COLUMN DOB Date;
ALTER TABLE Companies ADD COLUMN State varchar(30);
```

**Output:**

![image](https://github.com/user-attachments/assets/f2d62420-bd88-427d-84f1-592952369999)


**Question 7**
---
-- Insert all employees from Former_employees into Employee

Table attributes are EmployeeID, Name, Department, Salary

```sql
-- Insert into Employee (EmployeeID,Name,Department,Salary)
Select EmployeeID,Name,Department,Salary from Former_employees;
```

**Output:**

![image](https://github.com/user-attachments/assets/9690ebb7-9994-4790-9e75-a21fbbd3bedb)


**Question 8**
---
-- Create a table named Orders with the following columns:

OrderID as INTEGER
OrderDate as TEXT
CustomerID as INTEGER

```sql
-- create table Orders(
OrderID INTEGER,
OrderDate TEXT,
CustomerID INTEGER
);
```

**Output:**

![image](https://github.com/user-attachments/assets/bd495237-4b5a-4799-9aab-8985fd35b84a)


**Question 9**
---
-- In the Books table, insert a record where some fields are NULL, another record where all fields are filled without any NULL values, and a third record where some fields are filled, and others are left as NULL.

```sql
-- -- First record: Some fields are NULL
INSERT INTO Books (ISBN, Title, Author)  
VALUES ('978-1234567890', 'Introduction to AI', 'John Doe');

-- Second record: All fields are filled (no NULL values)
INSERT INTO Books (ISBN, Title, Author, Publisher, Year)  
VALUES ('978-9876543210', 'Deep Learning', 'Jane Doe', 'TechPress', 2022);

-- Third record: Some fields are filled, and others are NULL
INSERT INTO Books (ISBN, Title, Author, Year)  
VALUES ('978-1122334455', 'Cybersecurity Essentials', 'Alice Smith', 2021);

```

**Output:**

![image](https://github.com/user-attachments/assets/066e9b0c-f6d9-494f-aab8-8d1c7a037244)


**Question 10**
---
-- Write a SQL query for adding a new column named "email" with the datatype VARCHAR(100) to the  table "customer" 

Sample table: customer
 

```sql
-- ALTER TABLE Customer
ADD COLUMN email VARCHAR(100);
```

**Output:**
![image](https://github.com/user-attachments/assets/f0ce6b2e-0750-4b80-9876-9d2d16e6fcfb)
