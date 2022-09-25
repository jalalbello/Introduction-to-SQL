# Cross Join

Its rarely used, if we want to return a cartesian product we use it

## CTE 'Common Table expressions'

We are going to use a temp table to demonstrate our cross join

> Syntax :
> > WITH someName AS (
> >
> >{SQL here}
> >
> >)
> > 
> > Select *
> >
> > FROM someName
---
---
>Example :
>> - Two collumns SetA and SetB
>> - One has X - Y - Z
>> - The other has 1 2 3

```sql 
WITH SetA AS (
	SELECT 'X' AS A
	UNION ALL
	SELECT 'Y'
	UNION ALL
	SELECT 'Z'
)
, SetB AS (
	SELECT '1' AS B
	UNION ALL
	SELECT '2'
	UNION ALL
	SELECT '3'
)
SELECT A B
FROM SetA
```

### **Bonus Task**

Make the generated collumn shorter
```sql
WITH SetA AS (
	GENERATE_SERIES(1,3) AS A
)
, SetB AS (
	CHR(GENERATE_SERIES(88,90)) AS B
)
SELECT A B
FROM SetA
```

Lets use our **Cross** **Join** On the sets

> ! Cross joins do not use the ON operator, it has no purpuse for it

```sql
WITH SetA AS (
	SELECT 'X' AS A
	UNION ALL
	SELECT 'Y'
	UNION ALL
	SELECT 'Z'
)
, SetB AS (
	SELECT '1' AS B
	UNION ALL
	SELECT '2'
	UNION ALL
	SELECT '3'
)
SELECT A, B
FROM SetA
	CROSS JOIN SetB
```

Basicly what cross join does, it that it takes two tables, and creates an output that is a combination of both

>So how can it be **usefull** you may ask, here is a **hypothetical**
> 
> In our database we have 3 Stores, 3 Tasks 
> 
> We want to generate a table that has each store asigned to it each task, easy for us then to cross join and get that result, so 3 tasks and 3 stores become 9 stores 9 tasks
> 
> Also bonus point if we add a due date collumn that has a single string and we get have 9 stores 9 tasks 9 dates in the result of our cross join query


