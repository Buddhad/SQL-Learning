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

`Questions:1` Get all details for all French language films.

`Questions:2` Get the name and birth date of the person born on November 11th, 1974. Remember to use ISO date format ('1974-11-11')!

`Questions:3` Get the number of Hindi language films.

`Questions:4` Get all details for all films with an R certification.

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

`Questions:1` Get the title and release year for all Spanish language films released before 2000.

`Questions:2` Get all details for Spanish language films released after 2000.

`Questions:3` Get all details for Spanish language films released after 2000, but before 2010.

+ [`Answers`](../Answers/Ex-4.md)
