
<h1 style="color:darkblue;">DBMS Experiment 1</h1>

<h2 style="color:darkgreen;">Aim</h2>
To perform DDL and DML operations on the Employee table as per the given queries.

<h2 style="color:darkgreen;">Question 1</h2>
Create Employee_master table with data using Employee table.

<h3>Query</h3>

sql
CREATE TABLE Employee_master AS
SELECT * FROM Employee;


<h2 style="color:darkgreen;">Question 2</h2>
Delete all records from Employee_master whose DeptNo is 10.

<h3>Query</h3>

sql
DELETE FROM Employee_master
WHERE DEPTNO = 10;


<h2 style="color:darkgreen;">Question 3</h2>
Update 10% increase in the salary of employees belonging to DEPTNO 20 in Employee_master.

<h3>Query</h3>

sql
UPDATE Employee_master
SET SAL = SAL + (SAL * 0.10)
WHERE DEPTNO = 20;


<h2 style="color:darkgreen;">Question 4</h2>
Alter the SAL column to NUMBER(10,2) in Employee_master.

<h3>Query</h3>

sql
ALTER TABLE Employee_master
MODIFY SAL NUMBER(10,2);


<h2 style="color:darkgreen;">Question 5</h2>
Drop Employee_master table.

<h3>Query</h3>

sql
DROP TABLE Employee_master;<h1 style="color:darkblue;">

