# EXP NO 10: SYNONYMS AND ASSERTIONS IN SQL 
### DATE: 
## AIM:
To create a student database and create a synonym and assertions.

## THEORY
## SYNONYM
<div align="justify">
A SYNONYM provides another name for database object, referred to as original object, that may exist on a local or another server.
</div>
## ASSERTIONS
<div align="justify">
* An assertion is a piece of SQL which makes sure a condition is satisfied, else or it stops the action being taken on a database.
* An assertion is a constraint that might be dependent upon multiple rows of multiple tables.
</div>

## Query:
### 1) Create a table EMPLOYEE and perform insertion of two rows.

### SQL QUERY: 
```
CREATE TABLE EMPLOYEE (
    employee_id INT ,
    name VARCHAR(255),
    department VARCHAR(255),
    salary DECIMAL(10, 2)
);
```
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/8bc32804-2ad9-496c-85f0-f1381e1bc914)

### 2) Create a synonym S1 for EMPLOYEE  table.

### SQL QUERY:
```
CREATE SYNONYM S1 FOR EMPLOYEE;
```
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/70efa8ed-5b2e-4bb6-a9d3-1950a9d6fabb)

### 3) Display the EMPLOYEE  table using synonym S1.
 
### SQL QUERY: 
```
SELECT * FROM S1;
```
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/cd22c3bb-af10-4852-9b09-7b9a7992b296)

### 4) Drop the synonym.

### SQL QUERY: 
```
DROP SYNONYM S1;
```
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/e0a93f88-5584-4305-9b0a-9396e003be91)

### 5) Create a supplier table and create a sequence S2 for supplier table id.

### SQL QUERY: 
```
CREATE TABLE supplier (
    id INT,
    name VARCHAR(255),
    address VARCHAR(255),
    contact_person VARCHAR(255)
);

CREATE SEQUENCE S2 START 1;
```
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/1bd8289c-c074-44a6-8acc-09359589022e)

### 6) insert the data into supplier table use sequence.

### SQL QUERY: 
```
INSERT INTO supplier (id, name, address, contact_person)
VALUES (NEXTVAL('S2'), 'ABC Suppliers', '123 Main Street', 'John Doe');

INSERT INTO supplier (id, name, address, contact_person)
VALUES (NEXTVAL('S2'), 'XYZ Distributors', '456 Elm Road', 'Jane Smith');
```
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/04bd6f41-6fad-43cc-986f-f0096001e06e)

### 7) Drop the sequence

### SQL QUERY: 
```
DROP SEQUENCE S2;
```
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/714b5a35-ee03-4172-87e5-472757786b3b)

## RESULT :
### Thus the sequence and synonym created and used in SQL.
