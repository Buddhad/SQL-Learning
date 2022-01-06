# Exercise -4
## `Exercise -4.1`
## Simple filtering of text
Remember, the `WHERE` clause can also be used to filter text results, such as names or countries.

For example, this query gets the titles of all films which were filmed in China:
```sql
SELECT title
FROM films
WHERE country = 'China';
```
Now it's your turn to practice using `WHERE` with text values!

Important: in PostgreSQL (the version of SQL we're using), you must use single quotes with `WHERE`.

`Question: 1` Get all details for all French language films.

`Question: 2` Get the name and birth date of the person born on November 11th, 1974. Remember to use ISO date format ('1974-11-11')!

`Question: 3` Get the number of Hindi language films.

`Question: 4` Get all details for all films with an R certification.

+ [`Answers`](../Answers/Ex-4.md)

## `Exercise -4.2`
## WHERE AND
Often, you'll want to select data based on multiple conditions. You can build up your `WHERE` queries by combining multiple conditions with the `AND` keyword.

For example,
```sql
SELECT title
FROM films
WHERE release_year > 1994
AND release_year < 2000;
```

gives you the titles of films released between 1994 and 2000.

Note that you need to specify the column name separately for every `AND `condition, so the following would be invalid:

```sql
SELECT title
FROM films
WHERE release_year > 1994 AND < 2000;
```
You can add as many `AND` conditions as you need!

`Question: 1` Get the title and release year for all Spanish language films released before 2000.

`Question: 2` Get all details for Spanish language films released after 2000.

`Question: 3` Get all details for Spanish language films released after 2000, but before 2010.

+ [`Answers`](../Answers/Ex-4.md)

## `Exercise -4.3`

## WHERE AND OR
What if you want to select rows based on multiple conditions where some but not all of the conditions need to be met? For this, SQL has the `OR` operator.

`For example`, the following returns all films released in either 1994 or 2000:
```sql
SELECT title
FROM films
WHERE release_year = 1994
OR release_year = 2000;
```
### `Note:` You need to specify the column for every OR condition, so the following is invalid:

```sql
SELECT title
FROM films
WHERE release_year = 1994 OR 2000;
```

### When combining `AND` and `OR`, be sure to enclose the individual clauses in parentheses, like so:

```sql
SELECT title
FROM films
WHERE (release_year = 1994 OR release_year = 1995)
AND (certification = 'PG' OR certification = 'R');
```
`Question: 1` What does the OR operator do?

`Options:`

1. Display only rows that meet at least one of the specified conditions.

2. Display only rows that meet all of the specified conditions.

3. Display only rows that meet none of the specified conditions.

+ [`Answers`](../Answers/Ex-4.md)


## WHERE AND OR (1.1)

You now know how to select rows that meet some but not all conditions by combining AND and OR.

`For example`

The following query selects all films that were released in `1994 or 1995` which had a rating of `PG` or `R`.

```sql
SELECT title
FROM films
WHERE (release_year = 1994 OR release_year = 1995)
AND (certification = 'PG' OR certification = 'R');
```

`Question: 1 ` Get the title and release year for films released in the 90s.

`Question: 2 ` Now, build on your query to filter the records to only include French or Spanish language films.

`Question: 3 ` Finally, restrict the query to only return films that took in more than $2M gross.
