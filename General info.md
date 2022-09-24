# Info about sequel

Sql syntax is really easy, we are just telling the database what we want from it, and the data base will return that info within the parameters set by the query

This is refered to as Declerative programming

## Delecrative programming

In Delecrative programming we don't explain the how, we just ask for what we want, and it will find a path to what we need

## Most common sql queries

The most common are series of clauses that are written in a strict linear order

## Null Values

Values that do not exist are 'Null'

## SQL alias

An alias is a name we set for a column, table, or a fucntion in SQL

```sql
SELECT first_name, last_name, 
CONCAT(first_name, ' ', last_name) AS "Full Name"
FROM actor AS "a"
------------------- 
SELECT first_name, last_name, 
CONCAT(first_name, ' ', last_name) "Full Name"
FROM actor "a"
```
> USING SINGLE QUOTES FOR FULL NAME WONT WORK

## Referential integrity

A **vital** aspect of database design, Its the concept that refers to the acuracy and validity of the data that defines t he Relationships between SQL tables, **foreign key** constraints are a crucial component in maintaining Referential integrity, insuring we don't break any of our table relationships

## Orphaned Records

Rows with a foreign key, pointing to a record that no longer exist in the other table

## Filtering IN FROM vs in WHERE

When we filter in **from** we filter that data before the join, where is a filter that gets applied after the join

Always ask:
> When is this filter being applied to my data