# SQL Statement Fundamentals

## Challenges
### SELECT Statement
-- Use a SELECT statement to grab the first and last name names of every customer and their email customer. 

SELECT first_name, last_name, email FROM customer; 

### SELECT DISTINCT
-- Retrieve the distinct rating types our films could have in our database.

SELECT DISTINCT rating FROM film; 

### SELECT WHERE 
-- A customer forgot their wallet we need to track them down. What is the email for the customer Nancy Thomas?

SELECT email FROM customer
WHERE first_name = 'Nancy'
AND last_name = 'Thomas';

-- A customer wants to know the description for the movie "Outlaw Hanky".

SELECT description FROM film
WHERE title = 'Outlaw Hanky';

