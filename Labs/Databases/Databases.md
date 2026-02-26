## Performing a Conditional Search

In this lab, I worked with a relational database named world, which contains three tables:

- city
- country
- countrylanguage

The main objective of this lab was to practice writing SQL queries using the *SELECT*statement together with the *WHERE* clause to perform conditional searches. I connected to a **Command Host instance** on Amazon EC2 via the AWS Management Console and used a MySQL client to query the database.This hands-on exercise strengthened my understanding of filtering records, working with operators, and using SQL functions effectively.

## Lab Objectives

By completing this lab, I learned how to:

- Write search conditions using the WHERE clause

- Use the BETWEEN operator for range filtering

- Use the LIKE operator with wildcard characters

- Create column aliases using the AS keyword

- Apply aggregate functions in a SELECT statement

- Use functions within a WHERE clause


## Connecting to the Command Host

I began by accessing the AWS environment and navigating to Amazon EC2 through the AWS Management Console.

Steps I performed:

- Opened EC2 from the Services menu.

- Located the instance labeled Command Host.

- Connected using Session Manager.

Switched to the root user and navigated to the working directory:

sudo su
cd /home/ec2-user/

Connected to MySQL:
mysql -u root --password='re:St@rt!9'

After successfully connecting, I was ready to query the world database.


## Task 2: Querying the world Database
**Viewing Available Databases**

First, I verified that the world database existed:

SHOW DATABASES;


Then I explored the country table:
SELECT * FROM world.country;


## Using the WHERE Clause with AND

To filter countries with a population between 50 million and 100 million, I used:
SELECT Name, Capital, Region, SurfaceArea, Population
FROM world.country
WHERE Population >= 50000000 AND Population <= 100000000;

This helped me understand how multiple conditions can be combined using the  (AND) operator.

