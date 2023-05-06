# Exercise No 4

Note : To solve below queries use “spj” database

1. Display the PNAME and COLOR from the P table for the CITY=”London”.

        select Pname, color from p where city ='London';
----------------------------------------------------

2. Display all the Suppliers from London.

        select * from s where city = 'london';
----------------------------------------------------

3. Display all the Suppliers from Paris or Athens.

        select * from s where city In('paris','athens');
----------------------------------------------------

4. Display all the Projects in Athens.

        select * from j where city='Athens';
----------------------------------------------------

5. Display all the Part names with the weight between 12 and 14(inclusive of both).

        select * from p where weight between 12 and 14;
----------------------------------------------------

6. Display all the Suppliers with a Status greater than or equal to 20.

        select * from s  where status >= 20;
----------------------------------------------------

7. Display all the Suppliers except the Suppliers from London.

        select * from s where not city ='london';
----------------------------------------------------

8. Display only the Cities from where the Suppliers come from.

        select city from s;
----------------------------------------------------

9. Display the Supplier table in the descending order of CITY.

        select * from s order by city desc;
----------------------------------------------------

10. Display the Part Table in the ascending order of CITY and within the city in the ascending order of Part names.

----------------------------------------------------

11. Display all the Suppliers with a status between 10 and 20.

----------------------------------------------------

12. Display all the Parts and their Weight, which are not in the range of 10 and 15