---
Title: Nekocloud Migrations
---

## Nekocloud migrations
The migrations for Nekocloud (NC from now on) are completly constructed inside the database.  
Because all the migration code is written in plpgsql, it is only compatible with Postgresql for the DB.  


## Workings
The migrations work by creating the required tables, functions, procedures, etc... in a .sql file in the configured migrations folder.  
The filename should be of the format: yyyyMMddhhmmss-short-description.sql  
Then call the migration function with any postgres compatible client as the admin role, 
and it will read out all the .sql files in the migrations folder and execute them.
