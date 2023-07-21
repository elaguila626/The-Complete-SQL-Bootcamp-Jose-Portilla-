## TIME STAMP AND EXTRACT

-- During which months did payments occur? Format your answer to return back the full month name.  

SELECT 
<br> DISTINCT(TO_CHAR(payment_date,'MONTH')
<br> FROM payment

-- How many payments occurred on a Monday? 

SELECT COUNT(*)
<br> FROM payment
<br> WHERE EXTRACT(dow FROM payment_date) = 1; 

<b> -- A review of mathematical functions, subqueries, and self-joins was covered during this section as well.
