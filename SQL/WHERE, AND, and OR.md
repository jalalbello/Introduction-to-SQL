# WHERE, AND, and OR

In the following example we will query our data base so it returns only actors named Ben Willis, by using **where** and the comparison operator =, and the conditional statement **and**

```sql
SELECT actor_id, first_name, last_name
FROM actor
WHERE first_name ='Ben' AND last_name = 'Willis'
```

In this example we use OR, to get actors with first name Ben or Tom

```sql
SELECT actor_id, first_name, last_name
FROM actor
WHERE first_name ='Ben' OR first_name = 'Tom'
```

This strings are *case sensitive*, so be **carefull**

### Parentheses

**()** can be used to specify the order of our SQL, like this example where we return actors named Ben Willis, or Tom

```sql
SELECT actor_id, first_name, last_name
FROM actor
WHERE (first_name ='Ben' AND last_name = 'Willis') OR (first_name = 'Tom')
```

## VERY Important

Aggregate functions (Count or some) will not run in where

---
```sql
WHERE COUNT(*) > 1
!! ERROR !!
```