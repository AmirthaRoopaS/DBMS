# EX.NO 4 Data Control Language (DCL) Commands and Transaction Control Languages (TCL) in SQL
### DATE:
## AIM:
To create a manager database and execute DML queries using SQL.

# THEORY
## Data Control Language (DCL) commands
* Data control language (DCL) is used to access the stored data.
* It is mainly used for revoke and to grant the user the required access to a database.
## List of DCL commands: 
1. GRANT : It is used to insert data into a table.
2. REVOKE: It is used to update existing data within a table.
## Transaction control language(TCL) commands
1. COMMIT : COMMIT command in SQL is used to save all the transaction-related changes permanently to the disk
2. START TRANSACTION : to start the transaction
3. ROLLBACK : undo the transaction upto savepoint 
4. SAVEPOINT : create a savepoint to save the different parts of the same transaction using different names

### Q1) Create a table employee with employee id ,name and Address

### QUERY:
sql
create table employee(
emp_id numeric,
emp_name varchar(10),
addr varchar(40)
);
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/0658a38a-b2ef-4cfd-8eab-14f4d611abb4)

### Q2) Insert three rows into emploee table 


### QUERY:
sql
insert into employee values(1,'Luffy','EastBlue');
insert into employee values(2,'Shanks','GodValley');
insert into employee values(3,'Grap','MarinFord');
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/0543afeb-f174-4889-9c47-54ca77ef3cea)

### Q3) Start the transaction and create a save point s1.

### QUERY:
sql
savepoint A;
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/c401b46d-fc34-41b6-bf38-9acf4d91d67b)

### Q4) Perform insertion into employee table.

### QUERY:
sql
insert into employee(4,'Robin','EniesLobby');
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/470244c5-8769-42d1-b4ad-6eb17c63b225)

### Q6)	Display the employee table and create a save point s2 .


### QUERY:
sql
select * from employee;
savepoint s2;
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/b53ef840-45d1-4b7c-b8f1-7f98b357db1a)

### Q7)	Perform updation on any one of the row.


### QUERY:
sql
update employee set emp_name='Nico Robin' where emp_id=4;
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/81de07b4-97c6-4d49-82fd-2ee9d077ddf6)

### Q8) Display the employee table and rollback to  save point s2 


### QUERY:
sql
select * from employee;
rollback to s2;
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/fb835d11-8735-4aee-895d-95ae92c616cc)

### Q9) Display the employee table and commit the changes; 


### QUERY:
sql
select * from employee;
commit;
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/362121c3-ec4f-4987-861a-f00a47f35eb6)

### Q10) Rollback to save point s1;


### QUERY:
sql
rollback to A;
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/1162c5fb-87ff-4a4d-9839-9ce60aaa2b76)

### Q11)	Create a new user and grant access to any one database with "insert and update"


### QUERY:
CREATE USER new_user;
GRANT INSERT, UPDATE ON database_name TO new_user;
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/98b39685-715a-4122-9004-55a73fa13837)

### Q12) Check the user access and display the result 


### QUERY:
SHOW GRANTS FOR new_user;
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/40fc7982-66f7-4676-b1c1-7d516afadeae)

### Q13) Revoke the privillages.

### QUERY:
SHOW GRANTS FOR new_user;
REVOKE INSERT, UPDATE ON database_name FROM new_user;
SHOW GRANTS FOR new_user;
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/7a5c0fe8-f533-40c4-8397-e0cba795818b)

## RESULT :
Thus the basic TCL and DCL commands are executed.
