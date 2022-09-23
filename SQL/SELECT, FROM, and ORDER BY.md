# SELECT, FROM, and ORDER BY

## Openning the query tool from pg admin

We must first select the database.

Then we can right click and click query tool, or click the querry tool icon in the browser tab 

![](Query%20tool.png)

The tool has a tool bar

It also has an area that tells us what database we are using, aswell as the user, followed by the name of the server
Almost all queries will have a select clause and a from clause

## Select From

**Select** Tells the data base what we want displayed or returned in our query result

**From** Specifies where the data comes from
```sql
SELECT actor_id, first_name, last_name
FROM actor;
```
> The following code gives us the collumns ordered by actor_id
> > Because **actor_id** is a **primary key** 

## Order by

Since we do not want to order by actor ID, we will order by first name and last name to get an alphabetical order by them, we can use first name only, but it will not truly order the entire name

```sql
SELECT actor_id, first_name, last_name
FROM actor
ORDER BY first_name, last_name;
```
> the semi collon in this example came last, if it was next to from like previous example it would fail

### **desc**
```sql
SELECT actor_id, first_name, last_name
FROM actor
ORDER BY first_name DESC, last_name DESC;
```
> Same as last, but the DESC makes it that we get it in reverse order

### **Order by** *n*
```sql
SELECT actor_id, first_name, last_name
FROM actor
ORDER BY 2, 3;
```
> n stands for colum num, starts from 1
>> Order by first and last name

## Primary keys

Its a collumn that is unique for each table, in a well designed database, each table has its primary key that used to **uniquly** identify **each** row within it
