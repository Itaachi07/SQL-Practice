
# Exercise 07

Note : To solve below queries use “sales” database
1. Write a query that lists each order number followed by the name of the customer who made the order.

        select o.onum, c.cname from orders o inner join customers c on o.cnum=c.cnum; 
----------------------------------------------------
2. Write a query that gives the names of both the salesperson and the customer for each order along with the order number.

        select o.onum, c.cname, s.sname from orders o inner join customers c on o.cnum=c.cnum inner join salespeople s on s.snum=o.snum; 
----------------------------------------------------
3. Write a query that produces all customers serviced by salespeople with a commission above 12%. Output the customer’s name, the salesperson’s name, and the salesperson’s rate of commission.

        select c.cname, s.sname, s.comm from customers c inner join salespeople s ON c.snum=s.snum where comm>0.12;
----------------------------------------------------
4. Write a query that calculates the amount of the salesperson’s commission on each order by a customer with a rating above 100.

        select s.comm * o.amt as commision from orders o inner join salespeople s ON s.snum=o.snum inner join customers c ON s.snum=c.snum where c.rating>100;
----------------------------------------------------
5. Write a query that produces all pairs of salespeople who are living in the same city.Exclude combinations of salespeople with themselves as well as duplicate rows with the order reversed

----------------------------------------------------