1. Create user
	```sql
	CREATE USER user_name IDENTIFIED BY password
	DEFAULT TABLESPACE DATA
	TEMPORARY TABLESPACE TEMP
	QUOTA UNLIMITED ON DATA;
	GRANT CONNECT, RESOURCE to user_name; --Connection privilege
	```

2. Create role
	```sql
	CREATE ROLE ROL_EXAMPLE
```

3. Grant privilege
	```sql
	GRANT SELECT, INSERT, UPDATE, DELETE ON table_example TO USER;

```










# **Extra**
``` sql
SELECT 'GRANT SELECT, INSERT, UPDATE, DELETE ON ' || table_name || ' TO user_name;'
FROM user_tables;
```