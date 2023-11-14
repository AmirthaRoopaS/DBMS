# EXP NO 2: DATA DEFINITION LANGUGE COMMANDS 
### DATE
## AIM:
To create a student database and execute DDL queries using SQL.


## THEORY
### DDL (Data Definition Language)

* DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema.
* It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.
* DDL is a set of SQL commands used to create, modify, and delete database structures but not data.
* These commands are normally not used by a general user, who should be accessing the database via an application.

 
### List of DDL commands: 
1. CREATE: This command is used to create the database or its objects (like table, index, function, views, store procedure, and triggers).
2. DROP: This command is used to delete objects from the database.
3. ALTER: This is used to alter the structure of the database.
4. TRUNCATE: This is used to remove all records from a table, including all spaces allocated for the records are removed.
5. RENAME: This is used to rename an object existing in the database.

## Query:
### 1) Create a database studentdb

### SQL QUERY:
Create database studentdb;
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/08c3c5dc-a15a-4bb2-8c1d-f6f1f793f09a)

### 2) Create a table student  and insert any two rows with the following fieds RegisterNumber,Name,Age,Address,Phone number

### SQL QUERY: 
create table student(rollno int,name char(20),age int,address varchar(20),phoneno int);
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/02eb4ec9-6e8e-4ce5-bc3a-5e5604b94d21)

### 3) Alter the above student table by adding another attribute department

### SQL QUERY: 
alter table student add department char(30);
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/f7b01715-5a56-4d6a-8842-c8faa405b594)

### 4) Rename the student table to mystudent

### SQL QUERY: 
drop table student;
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/710b7334-2068-49f2-9a5c-6e6f25e81d45)

### 5) Delete the mystudent rows using truncate keyword

### SQL QUERY: 
truncate table student;
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/2f77b2c7-86c9-470b-bacc-2381429cbb5e)

### 4) Drop the mystudent table
 
### SQL QUERY: 
alter table student rename to mystudent;
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/093f435d-9b44-47c1-b464-c8bd98bdc0ca)

## Result:
         Thus the basic DDL commands in SQL are executed. 


