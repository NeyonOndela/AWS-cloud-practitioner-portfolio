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

<img width ="1000" height="500" alt="instance1" src= "https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/f539701a1b8ac42d21217a8286337145180e4c83/Resources/database1.jpg">


After successfully connected, I was ready to query the world database.


## Task 2: Querying the world Database
**Viewing Available Databases**

First, I verified that the world database existed:

SHOW DATABASES;


Then I explored the country table:
SELECT * FROM world.country;

<img width ="1000" height="500" alt="instance1" src="https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/f539701a1b8ac42d21217a8286337145180e4c83/Resources/database2.jpg">

<img width ="1000" height="500" alt="instance1" src="https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/0ee9785398c6e376dbdc97c33a981cac25775d6b/Resources/database3.jpg" />


## Using the WHERE Clause with AND

To filter countries with a population between 50 million and 100 million, I used:
SELECT Name, Capital, Region, SurfaceArea, Population
FROM world.country
WHERE Population >= 50000000 AND Population <= 100000000;

This helped me understand how multiple conditions can be combined using the  *AND* operator.

<img width ="1000" height="500" alt="instance1" src="https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/f539701a1b8ac42d21217a8286337145180e4c83/Resources/database4.jpg" />


## Using the BETWEEN Operator

To simplify the previous query, I used the BETWEEN operator:
SELECT Name, Capital, Region, SurfaceArea, Population
FROM world.country
WHERE Population BETWEEN 50000000 AND 100000000;

I learned that  *BETWEEN* is inclusive and makes range queries cleaner and easier to read.

<img width ="1000" height="500" alt="instance1" src="https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/f539701a1b8ac42d21217a8286337145180e4c83/Resources/database5.jpg ">



## Using the LIKE Operator and Wildcards

To search for countries in Europe, I used the *LIKE* operator with % wildcard characters:

SELECT SUM(Population)
FROM world.country
WHERE Region LIKE "%Europe%";

The % symbol allowed me to match any characters before or after the word "Europe".



<img width ="1000" height="500" alt="instance1" src= "https://github.com/NeyonOndela/AWS-cloud-practitioner-portfolio/blob/f539701a1b8ac42d21217a8286337145180e4c83/Resources/database6.jpg" />

## Using Column Aliases with AS

To make the output more readable, I added a column alias:
SELECT SUM(Population) AS "Europe Population Total"
FROM world.country
WHERE Region LIKE "%Europe%";

This improved the clarity of the result by renaming the calculated column.

## Using Functions in WHERE (Case Handling)

Although SQL is generally case-insensitive, I practiced using the LOWER() function to ensure consistent comparisons:

SELECT Name, Capital, Region, SurfaceArea, Population
FROM world.country
WHERE LOWER(Region) LIKE "%central%";

This taught me how to perform reliable string comparisons regardless of letter case.

## Conclusion


Through this lab, I gained practical experience in:

- Filtering data using conditional logic

- Writing clean and readable SQL queries

- Using aggregate functions like SUM()

- Improving result readability with aliases

- Handling case sensitivity using string functions

Overall, this lab improved my confidence in writing SQL queries for real-world database operations. now i understand how to perform conditional searches efficiently and how to manipulate and filter data using different SQL operators and functions.



