## GROUP BY

-- We have two staff members, with staff ID's 1 & 2. We want to give a bonus to the staff member that handled the most payments. 

SELECT staff_id, COUNT(amount)
<br> FROM payment
<br> GROUP BY staff_id

-- Corporate HQ is conducting a study on the relationship between replacement cost and a movie MPAA rating. What is the avg replacement cost per MPAA rating? 

SELECT rating, AVG (replacement_cost)
<br> FROM film
<br> GROUP BY rating;

-- We are running a promotion to reward our top 5 customers. What are the customer ids of the top 5 customers by total spend? 

SELECT customer_id, SUM(amount)
<br> FROM payment
<br> GROUP BY customer_id
<br> ORDER BY SUM(amount) DESC
<br> LIMIT 5; 

## HAVING
-- We are launching a platinum service for our most loyal customers. We will assign platinum status to customers that have had 40 or more transaction payments. What customer_id's are eligible for platinum status?

SELECT customer_id, COUNT(* )
<br> FROM payment
<br> GROUP BY customer_id
<br> HAVING COUNT (*) >= 40; 

-- What are the customer ids of customers who have spent more than $100 in payment transactions with our staff_id member 2?

SELECT customer_id, SUM(amount)
<br> FROM payment
<br> WHERE staff_id = 2
<br> GROUP BY customer_id
<br> HAVING SUM(amount) > 100; 

