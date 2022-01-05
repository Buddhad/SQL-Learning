# Answers Exercise 4
`Exercise -4.1`

1. 
```sql
select *
from films
where language='French'
```
2. 
```sql
select name,birthdate
from people 
where birthdate='1974-11-11'
```
3. 
```sql
select count(language)
from films
where language='Hindi'
```
4. 
```sql
select * from films
where certification='R'
```

`Exercise -4.2`

1. 
```sql
select title,release_year 
from films 
where language='Spanish'
and release_year<2000;
```
2. 
```sql
select * from films
where language='Spanish'
and release_year>2000
```
3. 
```sql
select * 
from films
where release_year> 2000 
and release_year<2010
and language='Spanish'
```
