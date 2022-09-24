# Column aliases and concatenation

## TASK: Combine two collumns first_name and last_name, and add space in between

```sql
SELECT first_name, last_name, 
CONCAT(first_name, ' ', last_name)
FROM actor
```
> ! White space added does not work with double quotes " ", SINGLE QUTOES ONLY