
<h1>DBMS Experiment 4</h1>

<h2>Aim</h2>
To perform date functions, string functions and salary calculation queries on Employee table.

<h2>Question 1</h2>
Display the list of employees who have joined the company before 30th June 1980 or after 31st December 1981.

<h3>Query</h3>

sql
SELECT *
FROM Employee
WHERE HIREDATE < TO_DATE('30-JUN-1980','DD-MON-YYYY')
OR HIREDATE > TO_DATE('31-DEC-1981','DD-MON-YYYY');


<h2>Question 2</h2>
Display the names of employees whose names have second alphabet A.

<h3>Query</h3>

sql
SELECT ENAME
FROM Employee
WHERE ENAME LIKE '_A%';


<h2>Question 3</h2>
Display the names of employees whose name is exactly five characters in length.

<h3>Query</h3>

sql
SELECT ENAME
FROM Employee
WHERE LENGTH(ENAME) = 5;


<h2>Question 4</h2>
Display the names of employees whose names have second alphabet A.

<h3>Query</h3>

sql
SELECT ENAME
FROM Employee
WHERE ENAME LIKE '_A%';


<h2>Question 5</h2>
Display the names of employees who are not working as salesman or clerk or analyst.

<h3>Query</h3>

sql
SELECT ENAME
FROM Employee
WHERE JOB NOT IN ('SALESMAN','CLERK','ANALYST');


<h2>Question 6</h2>
Display the name of the employee along with their annual salary (SAL*12). The employee earning highest salary should appear first.

<h3>Query</h3>

sql
SELECT ENAME, SAL*12 AS ANNUAL_SALARY
FROM Employee
ORDER BY SAL DESC;


<h2>Question 7</h2>
Display name, sal, hra, pf, da, total salary for each employee.

<h3>Query</h3>

sql
SELECT ENAME,
       SAL,
       SAL*0.15 AS HRA,
       SAL*0.05 AS PF,
       SAL*0.10 AS DA,
       (SAL + (SAL*0.15) + (SAL*0.10) - (SAL*0.05)) AS TOTAL_SALARY
FROM Employee;


<h2>Question 8</h2>
Update the salary of each employee by 10% increment who are not eligible for commission.

<h3>Query</h3>

sql
UPDATE Employee
SET SAL = SAL + (SAL*0.10)
WHERE COMM IS NULL;


<h2>Question 9</h2>
Display those employees whose salary is more than 3000 after giving 20% increment.

<h3>Query</h3>

sql
SELECT *
FROM Employee
WHERE (SAL + (SAL*0.20)) > 3000;


<h2>Question 10</h2>
Display those employees whose salary contains at least 3 digits.

<h3>Query</h3>

sql
SELECT *
FROM Employee
WHERE SAL >= 100;