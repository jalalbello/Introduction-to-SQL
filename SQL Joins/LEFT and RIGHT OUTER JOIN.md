## Task, get the name of the films Woddy Hoffman has stared in

```sql
SELECT
   first_name,
   last_name,
   film.title
FROM
   actor 
   LEFT OUTER JOIN
      film_actor 
      ON film_actor.actor_id = actor.actor_id 
   LEFT OUTER JOIN
   	   film
       ON film.film_id = film_actor.film_id
WHERE
   first_name = 'Woody' 
   AND last_name = 'Hoffman'
ORDER BY 3
```

In SQL Joins are written as part of the FROM clause, and most JOINS include the ON logical operator

These two mean the same thing

```sql
LEFT OUTER JOIN
LEFT JOIN
```

# Task, get all actors for a film title

```sql
SELECT
   first_name,
   last_name,
   film.title
FROM
   actor 
   LEFT OUTER JOIN
      film_actor 
      ON film_actor.actor_id = actor.actor_id 
   LEFT OUTER JOIN
   	   film
       ON film.film_id = film_actor.film_id
WHERE film.title = 'Snowman Rollercoaster'
ORDER BY 3
```