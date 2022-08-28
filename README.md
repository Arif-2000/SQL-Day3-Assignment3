# SQL-Day3-Assignment3

--Execution of Queries: -

--1. Retrieve a list of MANAGERS. 
select * from EMP where job='MANAGER'

--2. Find out the names and salaries of all employees earning more than 1000 per month. 
select ename,sal from EMP where sal>1000

--3. Display the names and salaries of all employees except JAMES. 
select ename,sal from EMP where ename!='JAMES'

--4. Find out the details of employees whose names begin with ‘S’. 
select * from EMP where ename like 'S%';

--5. Find out the names of all employees that have ‘A’ anywhere in their name. 
select ename from EMP where ename like '%A%'

--6. Find out the names of all employees that have ‘L’ as their third character in their name. 
select ename from EMP where ename like '__L%'

--7. Compute daily salary of JONES. 
select (sal/30) as 'Daily Salary' from EMP where ename='JONES'

--8. Calculate the total monthly salary of all employees. 
select sum(sal) as 'Total Salary' from EMP

--9. Print the average annual salary . 
select avg(sal*12) as 'Average Salary' from EMP

--10. Select the name, job, salary, department number of all employees except SALESMAN from department number 30. 
select ename,job,sal,deptno from EMP where job!='SALESMAN' or deptno!=30;

--11. List unique departments of the EMP table. 
select distinct(dname) from EMP inner join DEPT on EMP.deptno=DEPT.deptno;


--12. List the name and salary of employees who earn more than 1500 and are in department 10 or 30. Label the columns Employee and Monthly Salary respectively.
select ename as 'Employee',sal as 'Monthly Salary',deptno from EMP where (sal>1500) and (deptno=10 or deptno=30);

--13. Display the name, job, and salary of all the employees whose job is MANAGER or ANALYST and their salary is not equal to 1000, 3000, or 5000. 
select ename,job,sal from EMP where (job='MANAGER' or job='ANALYST') and (sal!=1000 or sal!=3000 or sal!=5000);

--14. Display the name, salary and commission for all employees whose commission amount is greater than their salary increased by 10%. 
select ename,sal,comm from EMP where comm>(sal+sal*0.10)

--15. Display the name of all employees who have two Ls in their name and are in department 30 or their manager is 7782. 
select ename from EMP where ename like '%Ls%' and deptno=30 or mgr_id=7782

--16. Display the names of employees with experience of over 10 years and under 20 yrs. Count the total number of employees. 


--17. Retrieve the names of departments in ascending order and their employees in descending order. 
select dname,ename from EMP join DEPT on EMP.deptno=DEPT.deptno order by dname asc,ename desc; 

--18. Find out experience of MILLER. 


