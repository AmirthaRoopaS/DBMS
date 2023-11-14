# EX 2 Data Manipulation Language (DML) Commands and built in functions in SQL
## AIM:
To create a manager database and execute DML queries using SQL.

# THEORY
## DML(Data Manipulation Language)
*  The SQL commands that deal with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements.
*  It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.

## List of DML commands: 
1. INSERT: It is used to insert data into a table.
2. UPDATE: It is used to update existing data within a table.
3. DELETE: It is used to delete records from a database table.
4. SELECT: The SELECT command shows the records of the specified table.

## Create the table as given below:
```sql
create table manager(enumber number(6),ename char(15),salary number(5),commission number(4),annualsalary number(7),Hiredate date,designation char(10),deptno number(2),reporting char(10));
```
## insert the following values into the table
```sql
insert into manager values(7369,'Dharsan',2500,500,30000,'30-June-81','clerk',10,'John');
insert into manager values(7839,'Subu',3000,400,36000,'1-Jul-82','manager',null,'James');
insert into manager values(7934,'Aadhi',3500,300,42000,'1-May-82','manager',30,NULL);
insert into manager values(7788,'Vikash',4000,0,48000,'12-Aug-82','clerk',50,'Bond');
```

### Q1) Update all the records of manager table by increasing 10% of their salary as bonus.

### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/eb660bd3-e277-4191-a716-04b4ca57868d)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/9c1c4ae8-5853-41b3-997f-291daa93aae5)

### Q2) Delete the records from manager table where the salary less than 2750.


### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/ecbfb94e-191b-453b-baac-3a16ed1c6e29)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/5fdeb487-1503-4729-a733-b9d7e0684e11)

### Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)


### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/f3835003-426d-4eee-af20-7cce7ca85eb1)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/c78e00ab-8c75-4747-9a8d-23478777416a)

### Q5)	List the names of Clerks from emp table.


### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/c7eeb6d9-3c1e-49bc-8c0d-d48a4233e16f)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/0387c6a1-4fe2-4e2f-afe6-7778dec608eb)

### Q6)	List the names of employee who are not Managers.


### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/5d10d1ec-2fb1-46f0-b272-ff13d3b5cefa)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/2b8b9481-fd71-4131-85c9-f1647667b58d)

### Q7)	List the names of employees not eligible for commission.


### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/7c03c91a-25d5-47b7-8e2d-9a9adf61729d)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/cfc7632f-8b1a-4fa0-87ce-223df8558109)

### Q8)	List employees whose name either start or end with ‘s’.


### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/0a7e4a63-c233-40d8-a6c2-59d3601a30ee)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/18c066d4-a6fb-4fcf-9ad6-d13a2566b7fd)

### Q9) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.


### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/268eff99-3dfa-480d-85e0-da46d6da2df1)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/3c8b6215-abd9-4686-9f4c-ec966dea4684)

### Q10) List the Details of Employees who have joined before 30 Sept 81.


### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/d63dbdc4-a92c-4fe1-8a2b-604189f705b8)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/c41e8ad6-1c9e-4adf-afbe-432cfd73d2c6)

### Q11)	List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.


### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/8188852b-411a-407a-b929-3cbb888676e0)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/44556823-4153-4a18-8b43-ee594caa48cf)

### Q12) List the names of employees not belonging to dept no 30,40 & 10


### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/1d1da4db-2c0e-430b-abd4-33426a3d103b)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/836666ee-be6c-439f-9d8d-0b518042121c)

### Q13) Find number of rows in the table EMP

### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/8e470b50-2ded-4272-8052-f6c0367d93c0)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/6dbc4a21-efe8-4c62-9a68-f91557a21f39)

### Q14) Find maximum, minimum and average salary in EMP table.

### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/77f2514c-e032-4be5-9071-a0663d60cc42)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/3a83b6cf-1a33-44e1-8660-311672cb6ef9)

### Q15) List the jobs and number of employees in each job. The result should be in the descending order of the number of employees.

### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/e3a82479-c059-431a-be16-4913980ce238)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/ed8b905c-dc65-400b-8080-a7a7c315d04b)

## RESULT :
Thus the basic DML commands are executed.
