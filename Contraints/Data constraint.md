## Foregein key constraints

A foreign key is a collumn or set of collumns, that creates a **RS** between two tables in SQL database .

They could also be called 'refrences'.

They **explicitly** state, this two tables are related to each other, using this or those collumns

Its suffixed with **fkey**

How to declare a contraint in SQL

```sql
 CREATE TABLE(
    CONSTRAINT ${} PRIMARY KEY (${})    
    CONSTRAINT ${} FOREIGN KEY (${})    
 )
```

Any Key can be composed of multiple collumns, it is known as a **composite** **key**

--- 

Ultimatly, key constraints help us keep the **intergrity** of our database

### Adding and Deleting Values from a table with constraints

![](fkey-pkey-table.png)

In this table wa cannot add actors to a film, unless we have database records for both the actors and the film

If we try to **delete** an *actor* from the *actor table*, postgres will return an error as it is **refrenced** by a fkey constraint
> We need to delete the all the film_actor records that refrence that actor

Ultimatly, Foreign key constraint help maintain the integrity of our data base

