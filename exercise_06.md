
# Exercise 06

Note : To solve below queries use “hr” database
1. Display manager ID and number of employees managed by the manager.

        select manager_id, count(employee_id) from employees group by manager_id; 

----------------------------------------------------
2. Display the country ID and number of cities we have in the country.

        select country_id, count(citay) from locations group by country_id;

----------------------------------------------------
3. Display average salary of employees in each department who have commission percentage.

        select department_id, avg(salary) from employees group by department_id;
        
        select d.department_name, avg(e.salary) from employees e inner join 
        departments d on e.department_id = d.department_id group by e.department_id;
----------------------------------------------------
4. Display job ID, number of employees, sum of salary, and difference between highest salary and lowest salary of the employees of the job.

        select job_id, count(employee_id), sum(salary), (max(salary)-min(salary)) as diff from employees group by job_id;

----------------------------------------------------
5. Display job ID for jobs with average salary more than 10000. 

        select job_id, avg(salary) as avgsal from employees group by job_id having avg(salary)>10000 ;

----------------------------------------------------
6. Display years in which more than 10 employees joined.

        select year(hire_date) from employees group by year(hire_date) having count(employee_id)>10;

----------------------------------------------------
7. Display departments in which more than five employees have commission percentage.

        select job_id from employees group by job_id having count(employee_id) >5;
----------------------------------------------------
8. Display employee ID for employees who did more than one job in the past.

        select * from employees ;

----------------------------------------------------
9. Display job ID of jobs that were done by more than 3 employees for more than 100 days.

----------------------------------------------------
10. Display department ID, year, and Number of employees joined. 

----------------------------------------------------
11. Display how many employees joined in each month of the current year.

----------------------------------------------------
12. Display details of departments in which the maximum salary is more than 1000

----------------------------------------------------