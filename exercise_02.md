
# Exercise No 2

Write the SELECT queries to do the following:-

Note : To solve below queries use “sales” database

1. Write a query that produces all rows from the Customers table for which the 
salesperson’s number is 1001.

_select * from customers where snum =1001;_
----------------------------------------------------
2. Write a select command that produces the rating followed by the name of each 
customer in San Jose.

_select rating, cname from customers where city='san jose';_
----------------------------------------------------
3. Write a query that will produce the snum values of all salespeople from the Orders 
table (with the duplicate values suppressed).

_Select Distinct snum from orders;_ 
----------------------------------------------------
4. Write a query that will give you all orders for more than Rs. 1,000.

select * from orders where amt>1000;

----------------------------------------------------
5. Write a query that will give you the names and cities of all salespeople in London with a commission above 0.10.

select sname, city from salespeople where city ='London' AND comm>0.10;

----------------------------------------------------
6. Write a query on the Customers table whose output will exclude all customers with a 
rating <= 100, unless they are located in Rome.
----------------------------------------------------
7. What will be the output from the following query?
Select * from Orders
where (amt < 1000 OR
NOT (odate = ‘1990-10-03’
AND cnum > 2003));
----------------------------------------------------
8. What will be the output of the following query?
Select * from Orders
where NOT ((odate = ‘1990-10-03’ OR snum >1006) AND amt >= 1500);
----------------------------------------------------
9. What is a simpler way to write this query?
Select snum, sname, city, comm from Salespeople
Where (comm >= .12 or comm <= .14);
----------------------------------------------------
10. Write a query that selects all of the customers serviced by Peel or Motika. 
(Hint:the snum field relates the two tables to one another).
----------------------------------------------------
11. Write a query that selects all orders except those with zeroes or NULLs in the amt 
field