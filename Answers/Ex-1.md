# Answers Exercise 1

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