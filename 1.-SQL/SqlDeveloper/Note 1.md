1. Create user
   ```sql
   CREATE USER USER_NAME IDENTIFIED BY PASSWORD
   DEFAULT TABLESPACE DATA
   TEMPORARY TABLESPACE TEMP
   QUOTA UNLIMITED ON DATA;
   GRANT CONNECT, RESOURCE TO USER_NAME--Connection privilege
   ```
   
2. Create Role
   ```sql
   CREATE ROLE ROL_EXAMPLE
   ```
   
3. Grant Privileges
   ```sql
   GRANT SELECT, INSERT, UPDATE, DELETE ON TABLE_NAME TO USER_NAME
   ```









# **Extra**
``` sql
SELECT 'GRANT SELECT, INSERT, UPDATE, DELETE ON ' || table_name || ' TO user_name;'
FROM user_tables;
```