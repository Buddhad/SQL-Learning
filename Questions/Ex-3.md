# Exercise -3
## `Exercise -3.1`

## Learning to `COUNT`

What if you want to count the number of `employees` in your `employees table`? 

The `COUNT()` function lets you do this by returning the number of rows in one or more columns.

For example, this code gives the number of rows in the people table:
```sql
SELECT COUNT(*)
FROM people;
```
`Questions:1` How many records are contained in the reviews table?


1. 9,468

2. 8,397

3. 4,968

4. 9,837

5. 9,864

+ [`Answers`](../Answers/Ex-3.md)
## `Exercise -3.2`
## Practice with COUNT
As you've seen, `COUNT(*)` tells you how many rows are in a table. However, if you want to count the number of non-missing values in a particular column, you can call `COUNT()` on just that column.

For example, to count the number of birth dates present in the `people` table:

```sql
SELECT COUNT(birthdate)
FROM people;
```

It's also common to combine `COUNT()` with `DISTINCT` to count the number of distinct values in a column.

For example, this query counts the number of distinct birth dates contained in the people table:
```sql
SELECT COUNT(DISTINCT birthdate)
FROM people;
```

`Questions:1` Count the number of rows in the people table.

`Questions:2` Count the number of (non-missing) birth dates in the people table.

`Questions:3` Count the number of unique birth dates in the people table.

`Questions:4` Count the number of unique languages in the films table.

`Questions:5` Count the number of unique countries in the films table.

+ [`Answers`](../Answers/Ex-3.md)

## `Exercise -3.3`

## Filtering 
In SQL, the `WHERE` keyword allows you to filter based on both text and numeric values in a table. 

There are a few different comparison operators you can use:
- = equal
- <> not equal
- < less than
- `>` greater than
- <= less than or equal to
- `>=` greater than or equal to

For example, you can filter text records such as title. The following code returns all films with the title 'Metropolis':
```sql
SELECT title
FROM films
WHERE title = 'Metropolis';
```
Notice that the WHERE clause always comes after the FROM statement!

**Note:- we will use <> and not != for the not equal operator, as per the SQL standard.**

`Questions:1` What does the following query return?

1. Films released before the year 2000

2. Films released after the year 2000
3. Films released after the year 2001
4. Films released in 2000

+ [`Answers`](../Answers/Ex-3.md)

## `Simple filtering of numeric values`
As you learned in the previous exercise, the `WHERE` clause can also be used to filter numeric records, such as years or ages.

For example, the following query selects all details for films with a budget over ten thousand dollars:
```sql
SELECT *
FROM films
WHERE budget > 10000;
```
Now it's your turn to use the WHERE clause to filter numeric values!

`Questions:1`  Get all details for all films released in 2016.

`Questions:2`  Get the number of films released before 2000.

`Questions:3`  Get the title and release year of films released after 2000.

+ [`Answers`](../Answers/Ex-3.md)

+ [`Back To The Beginners Page`](../SQL/Beginners.md)
