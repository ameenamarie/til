# SQL Snippets 
## Tests
Run this test before every PR
```sql
select my_primary_key from my_table
where my_primary_key is not null
group by 1
having count(*) > 1
```
