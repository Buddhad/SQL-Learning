# Answers Exercise 3
`Exercise -3.1`

1. 8,397

`Exercise -3.2`

1. 
```sql
select count(id) from people;
```
2. 
```sql
SELECT count(birthdate)
FROM people;
```
3. 
```sql
SELECT COUNT(distinct birthdate)
FROM people;
```
4. 
```sql
select count(distinct language) 
from films;
```
5. 
```sql
select count(distinct country)
from films;
```
`Exercise -3.3`

`Filtering `
1. *Films released after the year 2000*

1. 
```sql
select * from films
where release_year=2016
```
2. 
```sql
select  count(release_year )
from films
where release_year <2000
```
3. 
```sql
select title, release_year
from films
where release_year>2000
```


+ [`Back To The Question`](../Questions/Ex-2.md)