# Exercise No 5

Note : To solve below queries use “hr” database

1. Display first name and last name after converting the first letter of each name to upper case and the rest to lower case.

        select 
----------------------------------------------------
2. Display the first word in job title.

        select 
----------------------------------------------------
3. Display the length of first name for employees where last name contain character ‘b’ after 3rd position.

----------------------------------------------------
4. Display first name in upper case and email address in lower case for employees where the first name and email address are same irrespective of the case.

----------------------------------------------------
5. Display first name, salary, and round the salary to thousands.

        select first_name, round(salary,0) from employees;
----------------------------------------------------
6. Display employee ID and the date on which he ended his previous job.

        select employee_ID, hire_date as Last_day_of_previous_job from employees;
----------------------------------------------------
7. Display first name and date of first salary of the employees.

        select First_name, Date_add(Hire_date,Interval 1 Month)as First_salary_day from employees;
----------------------------------------------------
8. Display first name and experience of the employees.

        select e.first_name,  from employees e full join job_history jh on e.employee_id = jh.employee_id ;
----------------------------------------------------
9. Display first name of employees who joined in 2001.

        select first_name from employees where year(hire_date)=2001;
----------------------------------------------------
10. Display employees who joined in the current year.

        select * from employees where hire_date = year(now());
----------------------------------------------------
11. Display the number of days between system date and 1st January 2011.

        select datediff (now(),'2011-01-01');
----------------------------------------------------
12. Display number of employees joined after 15th of the month.

        select * from employees where day(hire_date) >15; 
----------------------------------------------------
13. Display third highest salary of employees

        select * from employees order by salary desc limit 2,1;

       
----------------------------------------------------