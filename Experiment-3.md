
<h1>DBMS Experiment 3</h1>

<h2>Aim</h2>
To perform sorting, pattern matching and salary calculation queries on Employee table.

<h2>Question 1</h2>
List all employees and jobs in Department 30 in descending order by salary.

<h3>Query</h3>

sql
SELECT ENAME, JOB
FROM Employee
WHERE DEPTNO = 30
ORDER BY SAL DESC;


<h2>Question 2</h2>
List job and Department Number of employees whose name are five letters long begin with 'A' and end with 'N'.

<h3>Query</h3>

sql
SELECT JOB, DEPTNO
FROM Employee
WHERE ENAME LIKE 'A___N';


<h2>Question 3</h2>
Display the name of employees whose name start with alphabet S.

<h3>Query</h3>

sql
SELECT ENAME
FROM Employee
WHERE ENAME LIKE 'S%';


<h2>Question 4</h2>
Display the names of employees whose name ends with alphabet S.

<h3>Query</h3>

sql
SELECT ENAME
FROM Employee
WHERE ENAME LIKE '%S';


<h2>Question 5</h2>
Display the names of employees working in department number 10 or 20 or 40 or employees working as clerks, salesman or analyst.

<h3>Query</h3>

sql
SELECT ENAME
FROM Employee
WHERE DEPTNO IN (10,20,40)
OR JOB IN ('CLERK','SALESMAN','ANALYST');


<h2>Question 6</h2>
Display employee number and names for employees who earn commission.

<h3>Query</h3>

sql
SELECT EMPNO, ENAME
FROM Employee
WHERE COMM IS NOT NULL;


<h2>Question 7</h2>
Display employee number and total salary for each employee.

<h3>Query</h3>

sql
SELECT EMPNO, (SAL + NVL(COMM,0)) AS TOTAL_SALARY
FROM Employee;


<h2>Question 8</h2>
Display employee number and annual salary for each employee.

<h3>Query</h3>

sql
SELECT EMPNO, SAL*12 AS ANNUAL_SALARY
FROM Employee;


<h2>Question 9</h2>
Display the names of all employees working as clerks and drawing a salary more than 3000.

<h3>Query</h3>

sql
SELECT ENAME
FROM Employee
WHERE JOB = 'CLERK'
AND SAL > 3000;


<h2>Question 10</h2>
Display the names of employees who are working as clerk, salesman or analyst and drawing a salary more than 3000.

<h3>Query</h3>

sql
SELECT ENAME
FROM Employee
WHERE JOB IN ('CLERK','SALESMAN','ANALYST')
AND SAL > 3000;