## JOIN 

-- California sales tax laws have changed and we need to alert our customers to this through email. What are the emails of the customers who live in California? 

SELECT district, email FROM customer
INNER JOIN address
ON address.address_id = customer.address_id
WHERE district = 'California'; 

-- A customer walks into and is a huge fan of actor 'Nick Wahlerg' and wants to know which movies he's in. Get all the moves that he's acted in. 

SELECT title, first_name, last_name
FROM film_actor INNER JOIN actor
ON film_actor.actor_id = actor.actor_id
INNER JOIN film 
ON film_actor.film_id = film.film_id
WHERE first_name = 'Nick'
AND last_name = 'Wahlberg'; 
