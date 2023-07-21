-- Return the customer IDs of customers who have spent at least $110 with the staff member who has an ID of 2.

SELECT customer_id,SUM(amount)
<br> FROM payment
<br> WHERE staff_id = 2
<br> GROUP BY customer_id
<br> HAVING SUM(amount) > 110;

-- How many films begin with the letter J?

SELECT COUNT(*) FROM film
<br> WHERE title LIKE 'J%';

-- What customer has the highest customer ID number whose name starts with an 'E' and has an address ID lower than 500?

SELECT first_name,last_name FROM customer
<br> WHERE first_name LIKE 'E%'
<br> AND address_id <500
<br> ORDER BY customer_id DESC
<br> LIMIT 1;
