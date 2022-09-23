# SELECT DISTINCT / COUNT / GROUP BY

## Task : Return a unique name from our data base

In order to do so, we will use **SELECT** **DISTINCT**

```sql
SELECT DISTINCT last_name
FROM actor
```

### **DISTINCT** Removes duplicate values from our results that are returned by our query

## Task : Use COUNT for unique names on our data base


### **Count** returns number of rows that meet a condition

```sql
SELECT COUNT(*)
FROM actor,
```

This returns number of rows in table actor

In order to select a collumn for a table, and run an aggregation against it(count in the following example), we must list that collumn in a GROUP BY clause

```sql
SELECT last_name, COUNT (*)
FROM actor
GROUP BY last_name
```

## Task : Find Most used last name
```sql
SELECT last_name, COUNT (*)
FROM actor
GROUP BY last_name
ORDER BY 2 DESC 
```