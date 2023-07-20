## GROUP BY

-- We have two staff members, with staff ID's 1 & 2. We want to give a bonus to the staff member that handled the most payments. 

SELECT staff_id, COUNT(amount)
<br> FROM payment
<br> GROUP BY staff_id

-- Corporate HQ is conducting a study on the relationship between replacement cost and a movie MPAA rating. What is the avg replacement cost per MPAA rating? 

SELECT rating, AVG (replacement_cost)
<br> FROM film
<br> GROUP BY rating;
