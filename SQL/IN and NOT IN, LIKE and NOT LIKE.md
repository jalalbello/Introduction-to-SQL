# IN and NOT IN, LIKE and NOT LIKE

## IN
```sql
SELECT actor_id, first_name, last_name
FROM actor
WHERE first_name IN ('Ben', 'Tom')
```

In is a logical operator, tests wether a condition is true 

Any logical can be reversed adding the **not** keyword

```sql
SELECT actor_id, first_name, last_name
FROM actor
WHERE first_name NOT IN ('Ben', 'Tom')
```

## LIKE

```sql
SELECT actor_id, first_name, last_name
FROM actor
WHERE lastname LIKE 'H%'
```

### **%**

This is a wild card operator, meaning anything can come after the H, we can combine it with another string to get (starts with), (endswith)

```sql
SELECT actor_id, first_name, last_name
FROM actor
WHERE last_name LIKE 'H%' and last_name LIKE '%s'
```
```sql
SELECT actor_id, first_name, last_name
FROM actor
WHERE last_name LIKE 'H%s'
```

We can also get (stars with), (contains in the middle)

```sql
SELECT actor_id, first_name, last_name
FROM actor
WHERE last_name LIKE 'H%pp%'
```



