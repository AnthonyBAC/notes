1. *Database*
	Set of data stored in a computer, usually structured in a way that makes the data easily accessible.

2. *Relational database*
	Type of database. Structure that allows us to identify and access data in relation to another piece of data. Data in relational database is organized into tables.

3. *Relational database management [RDBMS]*
	Program that allows you to create, update, and administer a relational database. Most relational database management systems use the SQL language to access the database.

4. *Structured Query Language [SQL]*
	Programming language used to communicate with data stored in a relational database.

5. *Constraints*
	Set of rules applied to the values of individual columns. They add information about how column can be used after a specifying the data type for a column.
		- PRIMARY KEY 
		- UNIQUE
		- NOT NULL
		- DEFAULT
		
		CREATE TABLE celebs (
		id INTEGER PRIMARY KEY,
		name TEXT UNIQUE
		grande INTEGER NOT NULL
		age INTEGER DEFAULT 10
		);

6. *Indexes*
	Powerful tool used in the background of databases to speed up queying.
	
```
CREATE INDEX customers_by_phone  
ON customers (phone_number)
```
