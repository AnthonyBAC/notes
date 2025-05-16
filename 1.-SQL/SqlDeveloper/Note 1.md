1. Create user (CLOUD)
   ```sql
   CREATE USER USER_NAME IDENTIFIED BY PASSWORD
   DEFAULT TABLESPACE DATA
   TEMPORARY TABLESPACE TEMP
   QUOTA UNLIMITED ON DATA;
   GRANT CREATE SESSION TO USER_NAME--Connection privilege
   ```
   
2. Create Role
   ```sql
   CREATE ROLE ROL_EXAMPLE;
   ```
   
3. Grant Privileges
   ```sql
   --General
   GRANT CREATE SESSION, SELECT, INSERT, UPDATE, DELETE ON TABLE_NAME TO USER_NAME;
   
   ```
   
   ```sql
   --Permisos tables 
   GRANT CREATE TABLE, CREATE SYNONYM, CREATE PUBLIC SYNONYM TO USER_NAME
   ```
   
4. Index
   ```sql
   CREATE INDEX IDX_NAME_INDEX ON TABLE(COLUMN_NAME)
   ```









# **Extra**
``` sql
SELECT 'GRANT SELECT, INSERT, UPDATE, DELETE ON ' || table_name || ' TO user_name;'
FROM user_tables;
```