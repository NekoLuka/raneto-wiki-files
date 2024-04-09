---
Title: General guidelines for DB objects
---

## Plpgsql functions and procedures
### Recommended clean code rules
1. Parameters have an p_ prefix and declared variables have an lv_ prefix so that it is easy to see what comes from where.

### General plpgsql structure
Procedure:
```sql
create [or replace] procedure procedure_name(parameter_list)
language plpgsql
as $$
declare
-- variable declaration
begin
-- stored procedure body
end; $$
```
Functions:
```sql
create [or replace] function function_name(parameter_list)
language plpgsql
as $$
declare
-- variable declaration
begin
-- stored function body
end; $$
```

## Handy links
- [Types of privileges](https://www.postgresql.org/docs/current/ddl-priv.html)
- [Default privileges](https://www.postgresql.org/docs/current/ddl-priv.html#PRIVILEGES-SUMMARY-TABLE)
- [Grammar for all diffrent grants](https://www.postgresql.org/docs/current/sql-grant.html)
- [All built-in default functions](https://www.postgresql.org/docs/current/functions-info.html)
- [List of exception codes and names](https://www.postgresql.org/docs/current/errcodes-appendix.html)
- [Grants layout](https://www.postgresql.org/docs/current/sql-grant.html)