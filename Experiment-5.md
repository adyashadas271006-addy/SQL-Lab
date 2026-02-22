
<h1>DBMS Experiment 5</h1>

<h2>Aim</h2>
To perform aggregate functions and built-in SQL functions on Employee table.

<h2>Question 1</h2>
Display the total number of employees working in the company.

<h3>Query</h3>

sql
SELECT COUNT(*) AS TOTAL_EMPLOYEES
FROM Employee;


<h2>Question 2</h2>
Display the total salary being paid to all employees.

<h3>Query</h3>

sql
SELECT SUM(SAL) AS TOTAL_SALARY
FROM Employee;


<h2>Question 3</h2>
Display the maximum salary from Employee table.

<h3>Query</h3>

sql
SELECT MAX(SAL) AS MAX_SALARY
FROM Employee;


<h2>Question 4</h2>
Display the minimum salary from Employee table.

<h3>Query</h3>

sql
SELECT MIN(SAL) AS MIN_SALARY
FROM Employee;


<h2>Question 5</h2>
Display the average salary from Employee table.

<h3>Query</h3>

sql
SELECT AVG(SAL) AS AVG_SALARY
FROM Employee;


<h2>Question 6</h2>
Display the maximum salary being paid to clerk.

<h3>Query</h3>

sql
SELECT MAX(SAL)
FROM Employee
WHERE JOB = 'CLERK';


<h2>Question 7</h2>
Display the maximum salary being paid in dept no 20.

<h3>Query</h3>

sql
SELECT MAX(SAL)
FROM Employee
WHERE DEPTNO = 20;


<h2>Question 8</h2>
Display the minimum salary paid to any salesman.

<h3>Query</h3>

sql
SELECT MIN(SAL)
FROM Employee
WHERE JOB = 'SALESMAN';


<h2>Question 9</h2>
Display the average salary drawn by managers.

<h3>Query</h3>

sql
SELECT AVG(SAL)
FROM Employee
WHERE JOB = 'MANAGER';


<h2>Question 10</h2>
Display the total salary drawn by analyst working in dept no 40.

<h3>Query</h3>

sql
SELECT SUM(SAL)
FROM Employee
WHERE JOB = 'ANALYST'
AND DEPTNO = 40;


<h2>Question 11</h2>
Display the names of the employee in Uppercase.

<h3>Query</h3>

sql
SELECT UPPER(ENAME)
FROM Employee;


<h2>Question 12</h2>
Display the names of the employee in Lowercase.

<h3>Query</h3>

sql
SELECT LOWER(ENAME)
FROM Employee;


<h2>Question 13</h2>
Display the names of the employee in Proper case.

<h3>Query</h3>

sql
SELECT INITCAP(ENAME)
FROM Employee;


<h2>Question 14</h2>
Display the length of your name using appropriate function.

<h3>Query</h3>

sql
SELECT LENGTH('Adyasha')
FROM DUAL;


<h2>Question 15</h2>
Display the length of all employee names.

<h3>Query</h3>

sql
SELECT ENAME, LENGTH(ENAME)
FROM Employee;