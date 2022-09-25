## TASK : see all films that a specific actor has starred IN 

```sql
SELECT
   first_name,
   last_name,
   film.title
FROM
   actor 
   INNER JOIN
      film_actor 
      ON film_actor.actor_id = actor.actor_id 
   INNER JOIN
   	   film
       ON film.film_id = film_actor.film_id
WHERE first_name = 'Woody' AND last_name = 'Hoffman'
ORDER BY 3
```

## TASK : return all actors that starred in the film 'Snowman Rollercoaster


```sql
SELECT
   first_name,
   last_name,
   film.title
FROM
   actor 
   INNER JOIN
      film_actor 
      ON film_actor.actor_id = actor.actor_id 
   INNER JOIN
   	   film
       ON film.film_id = film_actor.film_id
WHERE film.title = 'Snowman Rollercoaster'
ORDER BY 3
```

