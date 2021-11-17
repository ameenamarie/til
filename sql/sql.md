# SQL Snippets 
## Tests
Run this test before every PR
```sql
select my_primary_key from my_table
where my_primary_key is not null
group by 1
having count(*) > 1
```
## Snowflake tricks
For when you need to count something but don't want to write (case when <something> then 1 end)
```sql
count_if(<something>)
```
For when you want to include a list of patterns
  ```sql
  like any
  ```
