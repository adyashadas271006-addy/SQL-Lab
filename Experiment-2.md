<h1>DBMS Experiment 2</h1>

<h2>Aim</h2>
To perform various SELECT queries using Employee table.

<h2>Question 1</h2>
List all distinct jobs in Employee.

<h3>Query</h3>

sql
SELECT DISTINCT JOB
FROM Employee;


<h2>Question 2</h2>
List all information about employee in Department Number 30.

<h3>Query</h3>

sql
SELECT *
FROM Employee
WHERE DEPTNO = 30;


<h2>Question 3</h2>
Find all department numbers greater than 20.

<h3>Query</h3>

sql
SELECT DISTINCT DEPTNO
FROM Employee
WHERE DEPTNO > 20;


<h2>Question 4</h2>
Find all information about managers and clerks in department 30.

<h3>Query</h3>

sql
SELECT *
FROM Employee
WHERE DEPTNO = 30
AND JOB IN ('MANAGER', 'CLERK');


<h2>Question 5</h2>
List Employee name, Employee number and department of all clerks.

<h3>Query</h3>

sql
SELECT ENAME, EMPNO, DEPTNO
FROM Employee
WHERE JOB = 'CLERK';


<h2>Question 6</h2>
Find all managers not in department 30.

<h3>Query</h3>

sql
SELECT *
FROM Employee
WHERE JOB = 'MANAGER'
AND DEPTNO != 30;


<h2>Question 7</h2>
List information about all Employees in department 10 who are not manager or clerks.

<h3>Query</h3>

sql
SELECT *
FROM Employee
WHERE DEPTNO = 10
AND JOB NOT IN ('MANAGER', 'CLERK');


<h2>Question 8</h2>
Find Employees and jobs earning between 1200 and 1400.

<h3>Query</h3>

sql
SELECT ENAME, JOB, SAL
FROM Employee
WHERE SAL BETWEEN 1200 AND 1400;


<h2>Question 9</h2>
List Name and Department Number of employee who are clerks, analyst or salesman.

<h3>Query</h3>

sql
SELECT ENAME, DEPTNO
FROM Employee
WHERE JOB IN ('CLERK', 'ANALYST', 'SALESMAN');


<h2>Question 10</h2>
List Name and Department Number of employee whose names begin with M.

<h3>Query</h3>

sql
SELECT ENAME, DEPTNO
FROM Employee
WHERE ENAME LIKE 'M%';
