
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

----------------------------------------------------
4. Display job title, department name, employee last name, starting date for all jobs from 1993 to 1998.

----------------------------------------------------
5. Display job title and average salary of employees.

----------------------------------------------------
6. Display job title, employee name, and the difference between maximum salary for the job and salary of the employee.

----------------------------------------------------
7. Display last name, job title of employees who have commission percentage and belongs to department 30.

----------------------------------------------------
8. Display details of jobs that were done by any employee who is currently drawing more than 15000 of salary.

----------------------------------------------------
9. Display department name, manager name, and salary of the manager for all 
managers whose experience is more than 5 years.

----------------------------------------------------
10. Display employee name if the employee joined before his manager.

----------------------------------------------------
11. Display employee name, job title for the jobs employee did in the past where the job was done less than six months.

----------------------------------------------------
12. Display employee name and country in which he is working.

----------------------------------------------------
13. Display department name, average salary and number of employees with 
commission within the department.

----------------------------------------------------
14. Display the month in which more than 5 employees joined in any department located in Sydney.

----------------------------------------------------
15. Display employee name, job title, start date, and end date of past jobs of all employees with commission percentage null.

----------------------------------------------------