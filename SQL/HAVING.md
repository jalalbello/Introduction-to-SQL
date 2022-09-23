# HAVING

## Its a filter condition for data returned by the GROUP BY clause

### TASK : Get actors that have the same first name if they there is more than 3 of them in ascending order

```sql
SELECT first_name, COUNT(*)
FROM actor
GROUP BY 1 
HAVING COUNT(*)>3 
ORDER BY 1
```
