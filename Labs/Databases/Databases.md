## Performing a Conditional Search

In this lab, I worked with a relational database named world, which contains three tables:

- city
- country
- countrylanguage

The main objective of this lab was to practice writing SQL queries using the *SELECT*statement together with the *WHERE* clause to perform conditional searches. I connected to a Command Host instance on Amazon EC2 via the AWS Management Console and used a MySQL client to query the database.This hands-on exercise strengthened my understanding of filtering records, working with operators, and using SQL functions effectively.

## Lab Objectives

By completing this lab, I learned how to:

- Write search conditions using the WHERE clause

- Use the BETWEEN operator for range filtering

- Use the LIKE operator with wildcard characters

- Create column aliases using the AS keyword

- Apply aggregate functions in a SELECT statement

- Use functions within a WHERE clause


## Environment Setup

The lab environment included:

- An Amazon EC2 instance (Command Host)

- A MySQL database client

- A relational database named world

I connected to the Command Host via Session Manager and accessed the MySQL server using:
mysql -u root --password='re:St@rt!9'

To verify the database:
SHOW DATABASES;

To inspect the country table:
SELECT * FROM world.country;


## Conditional Queries Performed                
Filtering Records with WHERE and AND
To retrieve countries with populations between 50 million and 100 million:

