# Filtering with GREATER THAN LESS THAN NOT EQUAL BETWEEN

## Task

### Return all actors whose last name start with (W, X, Y, Z) 

```sql
SELECT actor_id, first_name, last_name
FROM actor
WHERE last_name > 'W'
```
This will return all last_names that are greater than W, But if we have someone nammed, John W, It will not return its name, cuz W is equal to W of course

Better solution below :

```sql
SELECT actor_id, first_name, last_name
FROM actor
WHERE last_name >= 'W'
```

## The unequal operator

## <> or !=

Example: 
```sql
SELECT actor_id, first_name, last_name
FROM actor
WHERE last_name <= 'Allen' AND first_name != 'Kim'
```

## Between

```sql
SELECT actor_id, first_name, last_name
FROM actor
WHERE last_name BETWEEN 'A' AND 'B'
```

This will return values greater than A and smaller than B, so no actual names with letter B will be returned

We can use C to get letters from Az to Bz
