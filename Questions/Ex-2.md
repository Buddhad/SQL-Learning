# Exercise -2
## `Exercise -2.1`

## `SELECT`ing single columns
While SQL can be used to create and modify databases, the focus of this course will be querying databases. A query is a request for data from a database table (or combination of tables). Querying is an essential skill for a data scientist, since the data you need for your analyses will often live in databases.

In SQL, you can select data from a table using a SELECT statement. For example, the following query selects the name column from the people table:
```sql
SELECT name
FROM people;
```
In this query, `SELECT` and `FROM` are called keywords. In SQL, keywords are not case-sensitive, which means you can write the same query as:

```sql
select name
from people;
```
That said, it's good practice to make `SQL keywords uppercase` to distinguish them from other parts of your query, like `column` and `table names`.

It's also good practice  to `include a semicolon at the end of your query`. This tells SQL where the end of your query is!

`Question: 1` Select the title column from the films table.

`Question: 2` Select the release_year column from the films table.

`Question: 3` Select the name of each person in the people table.
+ [`Answers`](../Answers/Ex-2.md)


## `Exercise -2.2`

## `SELECT`ing multiple columns
Well done! Now you know how to `select single columns`.The following `multi-step exercise` allows you to practice a new concept through repetition. Check it out!

In the real world, you will often want to s`elect multiple columns.` Luckily, `SQL` makes this really easy. To select `multiple columns` from a table, simply separate the column names with `commas`!

`For example,` this query selects two columns, name and birthdate, from the people table:

```sql
SELECT name, birthdate
FROM people;
```

Sometimes, you may want to `select all columns from a table`. Typing out every column name would be a pain, so there's a handy `shortcut:`

```sql
SELECT *
FROM people;
```

Before getting started with the instructions below, check out the column names in the `films table`!

`Question: 1` Get the title of every film from the films table.

`Question: 2` Get the title and release year for every film.

`Question: 3` Get the title, release year and country for every film.

`Question: 4` Get all columns from the films table.

+ [`Answers`](../Answers/Ex-2.md)

## `Exercise -2.3`

## `SELECT DISTINCT`
Often your results will include many duplicate values. If you want to select all the `unique values` from a column, you can use the `DISTINCT` keyword.

This might be useful if, for example, you're interested in knowing which `languages` are represented in the films table:

```sql
SELECT DISTINCT language
FROM films;
```
Remember, you can check out the data in the tables by `clicking on the table name!`

`Question: 1` Get all the unique countries represented in the films table

`Question: 2` Get all the different film certifications from the films table.

`Question: 3` Get the different types of film roles from the roles table.

+ [`Answers`](../Answers/Ex-2.md)


+ [`Back To The Beginners Page`](../SQL/Beginners.md)