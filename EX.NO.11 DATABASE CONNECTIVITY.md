# Ex. No: 10 DATA BASE CONNECTIVITY USING  MYSQL AND JAVA
### DATE: 
### AIM: To create database connectivity and display the employee table 

### Steps:
1. Install mysql,visual studio,jdk, extensions of java pack.
2. Create a employee table and insert the data into employee table  
3. Create a new java project in visual studio.
4. write a java progarm to perform the following 1.create a connection 2. fetch data and store it in result set 3. Display table rows. 4. Close the connection
5. Deploy the jar file in lib folder 
6. Run the program

### Program:
```
#PRGRAM TO CONNECT MYSQL AND PYTHON
#MENU DRIVEN PROGRAM

#To establish connection
import sys
import mysql.connector as mc
conn=mc.connect(host='localhost', user='root',passwd='1a2d8h12l',database='STUDENT')
cur=conn.cursor()

if conn.is_connected():
    print("Successfully connected to MySQL")
else:
    print("Could not connect to MySQL")

#INSERT INTO RECORD
def insert_rec():
    print("\nENTER RECORD DETAILS")
    refno=int(input("Enter register No: "))
    name=input("Enter Name: ")
    dept=input("Enter Department: ")
    yr=int(input("Enter Year of Study: "))
    R=(refno, name, dept, yr)
    qry="INSERT INTO STUDENT (REG_NO,NAME,DEPT,YEAR) VALUES (%s, %s, %s, %s)"
    cur.execute(qry,R)
    conn.commit()
    print("Record inserted successfully")
    return

#VIEW RECORD
def view_rec():
    print("\nFETCHING ALL RECORDS IN THE TABLE FOR VIEW")
    qry="SELECT * FROM STUDENT"
    cur.execute(qry)
    print("_______________________________________________")
    print("REGNO       NAME        DEPT       YEAR")
    print("_______________________________________________")
    data=cur.fetchall()
    for i in data:
        print(i[0],"\t",i[1],"\t",i[2],"\t",i[3])
    print("_______________________________________________")
    print("\nTotal no.of records = ",cur.rowcount)
    return

while(True):
    print("-"*60)
    print("           PYTHON-MYSQL CONNECTIVITY")
    print("         STUDENT RECORD MANIPULATION")
    print("-"*60)
    print("1. INSERT \n2. DISPLAY RECORD \n3. EXIT")
    ch=int(input("Enter the opertion's choice you want to perform[1-3] : "))
           
    if (ch==1):
           insert_rec()
    elif (ch==2):
        view_rec()
    else:
        print("Thank You !!")
        break
```




### Output:
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/f74e2e78-0782-4448-b0e4-36bc260626eb)
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/961db145-f95a-48e1-95f4-a91405363f96)
![image](https://github.com/DrUmaRaniV/DBMS/assets/143496311/23f93ea7-5de5-4854-ac1d-7323d24a7721)



### Result:
Thust the database is connected and data displayed sucessfully.
