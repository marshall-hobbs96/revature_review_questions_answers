# WEEK 3 REVIEW QUESTIONS
---
## DAY 1

<details> 
<summary> Click to expand </summary> 

1. What is an exception?
	- An exception is a special object that is throw whenever some kind of problem is encountered. For example, if we try 
	to open a file, and that file doesn't exist, we would get an exception. This exception would interrupt all other processes
	in the program, and if it isn't dealt with, will cause our program to terminate.
	
2. Are exceptions inherently bad? Why do we use them in applications?
	- Exceptions are not inherently bad. They provide us with a way to deal with unforseen issues coming up at runtime. They are useful
	for dealing with any of these unforseen issues, as they allow us to to set up responses to these kinds of scenarios so that they can 
	be dealt with in way that we would prefer, instead of just crashing our program. 
	
3. How can we relate throwing and handling exceptions to what should happen in our application when a user does something incorrectly? (ex. not using all inputs for the calculator app?)
	- What should happen in our application when a user does something wrong, is we should send some kind of output telling them that. Exceptions let 
	us do this by interrupting our program when it detects an issue, such as the wrong kind of input. Then we can catch this exception, and tell our program
	to print out a statement telling the user they input something wrong. Then we can continue with our program without it crashing. 
	
4. How do you handle exceptions?
	- By catching them in a catch block. 
	
5. What does "declaring" an exception mean? How is that different than handling (catching) an exception?
	- Declaring an exception means you mark that a method ***CAN*** throw an exception, without actually doing anything in that method to handle the 
	potential exception. This is different than simply handling an exception within the method, because it means that now whatever other applications
	call that method must deal with the possibility of a thrown exception instead. 
	
6. What is the difference between a checked and unchecked exception?
	- Checked exceptions are exceptions that can possibly be thrown during the course of the program and that the compiler forces you to deal with. If
	a checked exception is possible to be thrown from a method, and isn't caught by a catch block, then the compiler won't compile your code. An unchecked 
	exception, however, will be allowed to compile if there isn't a catch block to catch it. 
	
7. How do we create a custom checked exception?
	- To create a custom checked exception, we simply need to create a class that extends the Exception class. 
	
8. How do we create a custom unchecked exception?
	- To creata a custom unchecked exception, we simply need to create a class that extends the RunetimeException class.
	
9. If we have multiple catch blocks, should more specific exceptions come first or last?
	- More specific exceptions should be caught first. Otherwise, more specific exceptions would be caught in a more general catch block, and you would 
	neve reach the more specific catch block. 
	
10. What is the purpose of DBeaver?
	- The purpose of DBeaver is to provide us a simple way to interact with databases through SQL commands. 
	
11. Why did we install DBeaver and Postgres?
	- DBeaver: So we can communicate with any databases that we create (without having to create a custom application) 
	- Postgres: So we can run our own databases. 
	
12. What is JDBC?
	- JDBC stands for Java DataBase Connectivity. It is an API that is part of the Java Standard Library. It allows us an easy way to establish
	connections to databases within our java application. 
	
</details>
	
---

## DAY 2

<details> 
<summary> Click to expand </summary>

1. What does SQL stand for?
	- SQL Stands for Structured Query Language
	
2. Is SQL a programming language?
	- SQL is ***NOT*** a programming language. It doesn't contain any of the hallmarks of a programming language, such as loops, control statements, 
	etc. 
	
3. What is a relational database management system (RDBMS)?
	- A RDBMS is an actual system that implements relational databases. Relational databases are databases that utilize tables, rows, columns, etc. 
	PostgreSQL is an example of an RDBMS. 
	
4. What are common numerical datatypes we might use in SQL?
	- INTEGER: Whole numbers 
	- BIGINT: Big whole numbers
	- NUMERIC: Decimal numbers
	
5. What are common character types we might use?
	- VARCHAR(n): Variable number of characters, with a maximum on n 
	- CHAR(n): Fixed number of characters. Believe unused characters are "padded" automatically with space characters. A lot less efficient than VARCHAR
	
6. What are common date/time types we might use?
	- TIMESTAMP: Date/time
	- DATE
	- TIME
	
7. What is a schema?
	- The formal structure of the data and tables in a relational database. 
	- Refers to the collection of database objects in our database, such as tables, stored procedures, indices, sequences etc.
	
8. What SQL sublanguages are there?
	- DDL: Data Definition Language 
	- DML: Data Manipulation Language 
	- DQL: Data Query Lanaguage 
	- DCL: Data Control Language 
	- TCL: Transaction Control Language 
	
9. What commands are associated with DDL?
	- CREATE: Used to add new database objects (tables)
	- ALTER: Used to modify an existing table (add/remove column, change column name, change column datatype, etc.) 
	- TRUNCATE: Delete all data within a table without deleteing the table itself. 
	- DROP: Deletes the entire table
	
10. What commands are associated with DML?
	- INSERT: Insert a new record (row) into the table
	- SELECT: Retrieve data from a table
	- UPDATE: Update existing records in a table
	- DELETE: Delete a record in a table 
	
11. How is DQL related to DML? Which command from DML does DQL have?
	- DQL (Data Query Lanaguage) includes just SELECT. DQL is really just a sublanguage and/or alternate interpretation of DML.
	- Some people say SELECT is part of DML and DQL doesn't exist. Other people say SELECT belong ***JUST*** in DQL and DML doesn't 
	include SELECT

12. What does CRUD mean?
	- CRUD stands for Create, Read, Update, Delete. It is an acronym that stands for the four functions considered necessary to implement
	a persistent data storage application. 

13. What commands are associated with DCL?
	- GRANT: Grant permissions for users
	- REVOKE: Revoke permissions for users 

14. What commands are associated with TCL?
	- COMMIT: Commit all the DML commands passed since the last COMMIT, i.e. "make these changes permanent". Cannot rollback from this
	- ROLLBACK: Used to rollback changes made. Used to undo recent changes. Can't rollback before the last Commit
	- SAVEPOINT: Set checkpoints to ROLLBACK to. 

15. What are the 6 common constraints in SQL?
	- Constraints: restrictions we put on our columns within our tables. Restrict what kind of data we can put in the columns. 
	- PRIMARY KEY: Serves as a unique identifier for a record in a table. This value must be unique within the column. May not be NULL
	- FOREIGN KEY: Serves as a reference to a primary key in another table. Used to establish relationships between rows within different tables 
	- UNIQUE: Only unique values within this column are allowed. 
	- NOT NULL: Values in this column cannot be NULL
	- CHECK: Ensures that values within this column follows a certain condition, such as value must be greater than 0 
	- DEFAULT: Provides default values for entries within this column if a value is not provided when creating it. 

16. What are composite keys?
	- Composite keys are primary keys that are made up of more than one column. The combination of values from constituant columns must be unique

17. What is the purpose of database normalization?
	- To reduce redundency and duplicate data. Essentially to make our database more organized. 

18. What is 1NF?
	- Each table must have a primary key. 
	- Data should be atomic
		* Each piece of data should have its own column. For example, if someone has multiple cars, each car should get its own column, instead
		of concatonating together car1 and car2 together and putting them as a single piece of data into the car column 

19. What is 2NF?
	- Includes 1NF as well as...
	- No partial dependencies
		* If we use a composite key as our primary key, then a table must include all columns required to create that composite key. 
		* This also means if we don't use a composite key (just use a primary key) then we are automatically 2NF

20. What is 3NF?
	- Includes 2NF as well as...
	- No transitive dependencies	
		* A column cannot describe another column that then holds the primary key

21. What are the 3 relationships that describe multiplicity/cardinality?
	- 1 to 1
		* records in one table are associated with only 1 other record in another table
	- 1 to many
		* Each record in a table can be associated with many records in another table, while those records in another table are still
		only associated with the one record in the original table 
		* How our database must work in project 0. A client can have many different accounts associated with them. Therefore, there must 
		be a 1 to many relationship between clients and their accounts.
	- Many to Many
		* Each record in a table can be associated with many records in another table, and those records can have many associations with 
		records in the original table. 
		* This would apply if we could have joint bank accounts in project 0. Which you could do, if you wanted to go above and beyond the 
		project requirements. 

22. What is the SERIAL datatype in Postgres?
	- SERIAL is a special numeric type in Postgres. It labels a column as accepting integer types that will autoincrement as rows are added. 
	Convenient for a PRIMARY KEY column 

23. What does utility class mean?
	- A serial class is a name we use to describe a class whose primary purpose is to provide us with useful methods to use. They aren't intended
	to be instantiated and instead house useful static methods for our use. 

24. What steps do we need to take to query data from the database using the JDBC API in Java?
	- First we need to establish a connection with our database. We do this by creating a Connection object and passing the database URL, our
	username, and our password to the database. 
	- Next, we need to prepare a SQL statement (in string form) 
	- Lastly, we pass this SQL query to our database and receive our response, which we can then manipulate. 

25. What are the three layers?
	- Controller layer
		* interacts with our frontend/endpoints
		* Parses HTTP information to pass to Service layer
	- Service layer
		* Performs logic on whatever information is passed to it from the controller layer. This is the layer that does meaningful calculations
		and what not
		* If needed, interacts with the DAO layer in order to interact with our database (if we have one)
	- DAO/DAL layer
		* Interacts with our database. Performs CRUD operations with our database. 

26. What is the purpose of the data access layer?
	- So that we can perform CRUD (Create, Read, Update, Delete) with our database. 

</details>