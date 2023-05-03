
# Exercise No 3

Note : To solve below queries use “hr” database

1. Write a query to get unique department ID from employee table.

        select distinct department_id from employees;

----------------------------------------------------

2. Write a query to get all employee details from the employee table order by first name, descending.

        select * from employees order by first_name desc limit 10;

----------------------------------------------------

3. Write a query to get the employee ID, names (first_name, last_name), salary in ascending order of salary.

        select employee_id, concat(first_name, last_name) as Name, salary from employees limit 15; 

----------------------------------------------------

4. Display first name and join date of the employees who is either IT Programmer or Sales Man.

        select First_name, hire_date from employees where department_id IN (60,80) limit 15;

----------------------------------------------------

5. Display details of employee with ID 150 or 160.

        select * from employees where employee_id = 150 OR employee_id =160 ; 
        
----------------------------------------------------

6. Display first name, salary, commission pct, and hire date for employees with salary less than 10000.

        select first_name, salary, commission_pct, hire_date from employees where salary <10000;

----------------------------------------------------

7. Display employees where the first name or last name starts with S.

        select first_name, last_name from employees where first_name like 's%' or last_name like 's%';

----------------------------------------------------
8. Display details of jobs in the descending order of the title.

        select * from jobs order by job_title desc;
        
----------------------------------------------------

9. Display details of the employees where commission percentage is null and salary in the range 5000 to 10000 and department is 30.

----------------------------------------------------

10. Display employees first_name,email who are working in “Executive” department.

----------------------------------------------------

11. Display unique contry_id from locations table.

----------------------------------------------------

12. Display all employees whose have job_id IT_PROG and FI_ACCOUNT.

----------------------------------------------------

13. Display all countries in ascending order