
# Exercise 07 Optionl

Use appropriate joins to solve following queries.
Note : To solve below queries use “hr” database

1. Display department name and manager first name.

        select e.first_name, d.department_name from employees e inner join departments d ON e.department_id = d.department_id;
----------------------------------------------------
2. Display department name, manager name, and city.

    select d.department_name,concat(e.first_name,e.last_name ), l.city from departments d left join employees e  ON e.employee_id = d.manager_id inner join locations l ON l.location_id =d.location_id ;
----------------------------------------------------
3. Display country name, city, and department name.
    select c.country_name, l.city, d.department_name from countries c left join locations l on c.country_id = l.country_id left join departments d ON l.location_id = d.location_id ;

----------------------------------------------------
4. Display job title, department name, employee last name, starting date for all jobs from 1993 to 1998.

    select * from departments;
----------------------------------------------------
5. Display job title and average salary of employees.

        select job_id , avg(salary) from employees group by job_id;
----------------------------------------------------
6. Display job title, employee name, and the difference between maximum salary for the job and salary of the employee.

        
----------------------------------------------------
7. Display last name, job title of employees who have commission percentage and belongs to department 30.

        select last_name, job_id from employees where department_id = 30 AND commission_pct >0;
----------------------------------------------------
8. Display details of jobs that were done by any employee who is currently drawing more than 15000 of salary.

        select * from employees where salary > 15000;
----------------------------------------------------
9. Display department name, manager name, and salary of the manager for all 
managers whose experience is more than 5 years.


----------------------------------------------------
10. Display employee name if the employee joined before his manager.

----------------------------------------------------
11. Display employee name, job title for the jobs employee did in the past where the job was done less than six months.

----------------------------------------------------
12. Display employee name and country in which he is working.

        select e.first_name, c.country_name from employees e 
        left join departments d ON  e.department_id  = d.department_id  
        left join locations l ON d.location_id = l.location_id 
        left join countries c ON l.country_id = c.country_id limit 10;
----------------------------------------------------
13. Display department name, average salary and number of employees with 
commission within the department.

        select department_id , avg(salary), count(employee_id) from employees group by department_id; 
----------------------------------------------------
14. Display the month in which more than 5 employees joined in any department located in Sydney.


----------------------------------------------------
15. Display employee name, job title, start date, and end date of past jobs of all employees with commission percentage null.

----------------------------------------------------