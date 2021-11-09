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

---

## Day 3 

<details>

<summary> click to expand </summary>

1. What is a DTO (Data transfer object)?
	- An an object that satisfies the Java Bean standard. Used to encapsulate and pass around data as a single object. 
	- A ***MODEL*** is a type of DTO. It has all the properties associated with its database representation. 
	
2. What was the motivation for creating a AddOrUpdateStudentDTO class to use when adding or updating a student in our demo example?
	- In order to simplify and streamline our code. Using the AddOrUpdateStudentDTO allows us to self comment to a degree, as well as create an 
	object we can use for data transfers that only includes the properties we need. 
	
3. When we insert a new record, if the datatype for the primary key is SERIAL, do we need to provide a primary key value ourselves?
	- No we do not. Because it is a SERIAL type, it will auto increment when we insert a new entry. However, we can still assign our own values
	if we desire. This value doesn't need to be unique just because it is serial, but if we use a constraint such as PRIMARY KEY, then our value
	must be unique. This may create problems if we insert a serial number that the SERIAL sequence hasn't reached yet. I actually don't know, 
	something I may have to look up. 
		* For example, if we have id SERIAL PRIMARY KEY, and we already have id's 1, 2, 3 and 4 in our database, if we manually insert 5 in our database
		without letting SERIAL auto increment, will SERIAL auto increment into 5 next time we insert an entry without a specified id? I'll have to do
		some research. 
			- Serial will autoincrement into 5, thus causing an error. Credit to Jymm Enriquez for looking into that. 
			
4. What layer's methods will the service layer's methods be invoking?
	- The service layer's methods will be invoking methods from the Data Access Layer
	
5. What layer's methods will the controller layer's methods/lambdas be invoking?
	 - The Controller Layer's methods will be invoking the methods from the Service Layer
	 
6. What technology do we use in the controller layer (starts with J)?
	- Javalin
	
7. What technology do we use in the data access layer (also starts with a J)?
	- JDBC
	
8. What does `ctx.bodyAsClass(EditFirstNameDTO.class)` do in the demo's controller layer?
	- This pulls data from a JSON file sent to our database. It will create an object out of this data, and set the corrosponding properties 
	sent on the JSON to the properties of the object made. 
	- In this example, it will create a "EditFirstNameDTO" object, and set whatever properties were listed in the JSON to the corrosponding 
	(same named) properties in the new object. It will return an EditFirstNameDTO object.
	
9. What does `ctx.pathParam("id")` do in the demo's controller layer?
	- This pulls the information contained in the URI that is denoted as {id}. for example: localhost:8080/student/{id}/
		* ctx.pathParam("id") will pull whatever values is put into the {id} field whenever a request is sent to this url/uri 


</details>

---
## Day 4 

<details>

<summary> Click to expand </summary> 

1. What is the purpose of `ctx.json(...)`?
	- This is used to send back information to the HTTP client in JSON format. For example, if they wanted to create a new client for our banking
	application, we could send back information that confirms that it was a success, as well as provide information on the new client that was created. 

2. What is the purpose of `ctx.status(...)`?
	- This is to send HTTP status codes back to the HTTP client. This allows us inform the user about the status of their HTTP request. For example, if 
	something went wrong, we could send back a 4xx or 5xx error code, in order to better inform the user what exactly went wrong. Conversely, if 
	everything went right, we could send back a 2xx code to inform them of what successful action just took place. 
	
3. What is HTTP?
	- HTTP stands for HyperText Transfer Protocol. It is the standard protocol for communicating over the internet. It is composed of different 
	kinds of requests and responses. 
	
4. Describe the HTTP request/response cycle in relation to our backend application
	- A client (in our case, something like postman) sends an HTTP request containing information like what we would like to do (POST, GET, etc.)
	as well as any pertinent information. Once our server receives this information, we manipulate it and/or perform some action, and return some 
	kind of information back. This could either be information from our database that the client requested, or confirmation that we added new 
	information to our database. 
	
5. What are the 5 commonly used HTTP methods?
	- POST, GET, PUT, PATCH, DELETE
	
6. What is the proper usage of GET v. POST v. PUT v. PATCH v. DELETE?
	- PUT: Replace an entire resource, such as replacing the information of an entire banking client 
	- POST: Create a new resource, such as creating a new banking client
	- GET: Retrieve information on an existing resource, such as information on a current banking client
	- PATCH: Partially update information on an existing resource
	- DELETE: Completely delete an existing resource
	
7. What 4 components does an HTTP request consist of?
	- The HTTP method, which includes (but is not limited to) the five common HTTP methods just listed
	- URI (Uniform Resource Identifier). This looks like an extension of the URL, but actually contains additional information that is 
	passed to the server
	- Request headers. 
	- Request body.
	
8. What 3 components does an HTTP response consist of?
	- Status code. This is a short numerical code that gives a general status of the HTTP request just sent. Includes success and error codes
	- Response headers.
	- Response  body.
	
9. What do each of the 1XX, 2XX, 3XX, 4XX, and 5XX status code categories mean?
	- 1xx: Informational codes. 
	- 2xx: Successful codes. Used when an HTTP request is successful. Optionally provides a little more specific information about what that 
	successful request accomplished. 
	- 3xx: Redirection codes. Used to redirect in case of an endpoint or website moving, or some other such reason for a redirect. 
	- 4xx: Client error codes. Something is wrong on client end. Maybe you put the URL wrong, or tried to access something you don't have
	permissions for.
	- 5xx: Server error codes. Something bad happened on the server side, but it isn't the client's fault. 
	
10. If I wanted to delete a student with ID of 1, what is the appropriate HTTP method to use, and what might the URI look like?
	- If we're following the example give in lecture...an appropriate HTTP method would be DELETE. We would likely have a URI that looks
	something like "/students/1/deleteStudent". The "1" in this URI represents the ID of the student we wish to delete. 
	
11. What is referential integrity?
	- Referential integrity is the idea that we cannot have foreign keys that point to nothing. For example, if we had a clients and an accounts 
	table in our database, and the accounts table had a foreign key that linked accounts to a specific client, we couldn't drop our clients table, 
	because then we would have entries within the accounts table that would be referencing entries in the clients table that no longer exists. 
	This is the idea of referential integrity. We cannot delete entries that are being relied on by other entries, without first deleting the 
	entries that are doing the relying....If thats not too confusing to follow.....
	
12. What are the 4 ACID properties?
	- Atomicity
	- Consistency
	- Isolation
	- Durability
	
13. What is atomicity?
	- A transaction succeeds in its entirety or not at all. No partial transactions can occur. 
	
14. What is consistency?
	- A transaction cannot violate constraints or referential integrity.
	
15. What is isolation?
	- Two transactions cannot interfere with each other if they are happening concurrently. 
	
16. What is durability?
	- When a transaction is committed, it is permanently stored in database's memory. 
	
17. What are aggregate functions and scalar functions? How are they different from each other?
	- Scalar functions are functions that act on just one entry's information. Aggregate functions work on multiple entries information and 
	collates that data. 
	
18. Research and remember some examples of aggregate functions
	- SELECT AVG(funds) FROM clients. This is an aggregate function, because it aggregates all the results (funds) from all clients into one
	value, which in this case will be the average of all those funds. 
	
19. Research and remember some examples of scalar functions
	- SELECT name FROM clients. This will return the names of all clients within a clients table. It is scalar because for each entry, it is
	just acting on that entry alone, and returning a value for that one entry. 
	
20. What is the purpose of the GROUP BY clause? What type of function (scalar? aggregate?) do we use with GROUP BY?
	- Group by allows us to group our output by a certain criteria. This is used with aggregate functions. 
	
21. What is the difference between WHERE and HAVING?
	- WHERE would be used to filter out data by individual entries. HAVING would filter out aggregate data we've already collected. 
	
22. What are the 4 types of joins?
	- INNER JOIN
	- OUTER JOIN
	- LEFT JOIN 
	- RIGHT JOIN
23. How would you describe an INNER JOIN, an OUTER JOIN, a LEFT JOIN, and a RIGHT JOIN?
	- INNER JOIN: Joins from both tables if there are matching values in both tables
	- OUTER JOIN: Joins from either table if there are matchings in either table 
	- LEFT JOIN: Returns all records from the first table, as well as any matching records in the second table 
	- RIGHT JOIN: Returns all records from the second table, as well as any matching records in the first table
	
24. Of the following clauses associated with the SELECT command (`FROM`, `JOIN ... ON ... = ...`, `WHERE`, `GROUP BY`, `HAVING`, `ORDER BY`) remember the order they must be written in
	- Its listed in order in the question
	- FROM, JOIN ON, WHERE, GROUP BY, HAVNG, ORDER BY 
	
25. How does ORDER BY order the data from a query by default (ascending? descending?) ? How do we have it do the opposite?
	- By default, it orders it ascending (Smallest value at the top). If we want it to be deescending, we use DESC after the criteria we 
	want to order by. This will order it the opposite way, with the largest values at the top. 

</details> 

---

## DAY 5

<details>

<summary> Click to expand </summary> 

1. What are the classes and interfaces associated with the JDBC API?
	- DriverManager class
	- SQLException class
	- Connection Interface
	- Statement Interface
	- PreparedStatement Interface
	- CallableStatement Interface
	- ResultSet Interface
	
2. How does the DriverManager class help us to obtain a Connection object?
	- Allows us to register a database driver. This essentially lets the JDBC API know what kind of database its working with. We need to 
perform this step before we actually establish the connection with our database and obtain a Connection object	
	
3. What steps do we need to take to create a Connection object using DriverManager?
	- Once weve registered our drivermanager, we just need to provide the URL of our database, our username, and our password in order to 
	gain access. This is done by...Connection connection = DriverManager.getConnection(String url, String username, String password);
	
4. What is a SQL Driver? Why do we need to register the Postgres Driver with the DriverManager?
	- An SQL driver is a piece of software that we use to actually communicate to and from our database. We pass SQL statements to the driver
	and it sends these SQL statements to our database. It also handles any return messages the database wants to send to us. 
	- We need to register our postgres driver with the DriverManager because all SQL drivers are different, and thus will have different 
	acceptable ways to communicate with them. We must let our DriverManager know what SQL driver we're using so that it knows how to properly
	communciate with it. 
	
5. How is PreparedStatement different than Statement?
	- Statement generally just takes in any String that you pass to it. You can then call executeQuery or some other method that will then make 
	it send that string as an SQL statement to the database through the SQL driver. 
	- PreparedStatement does the same thing, however, instead of taking any String you pass to it, you instead premake a String with certain
	words missing in it, which you later fill in. These words are usually filled in as arguments gathered from a client. In this way, you can 
	have only predefined SQL statements that will wrap any user input, no matter how convuluted. In this way, you can prevent users from
	inputting their own custom SQL statements and therefore potentially carrying out SQL injection attacks. 
	
6. What do we use ResultSet for?
	- ResultSet stores any resulting data from our database that we may receive as a result of sending a SQL statement. It will store this data as 
	a separate object for each row. We can then iterate over each row given to us by using the .next() method, which returns true until it 
	reaches the end of rows to iterate over, in which case it will return false. 
	
7. What 2 common types of web services are in use today?
	- SOAP: Simple Object Access Protocol
	- REST: REpresentable State Transfer
	
8. What is REST?
	- REpresentable State Transfer. Its a modern paradigmn/design philosophy for modern web applications. Centered around using HTTP requests
	and responses in order to transfer data via JSON. Main goal is to be lightweight, maintainable, scalable. 
	
9. What are the 6 constraints of REST?
	- Stateless
		* The server should not save information about the previous request. Essentially, the properties and behaviors of our server shouldn't 
		change if we want to maintain a stateless server. If a client sends an http request, sending that http request shouldn't "lock" or "unlock"
		certain methods or properties of the server. 
		* This is more of a soft rule, because if we want to have things like logins, then we will likely have to violate this stateless constraint. 
		
	- Cacheable
		* The server should have the ability to cache data that is frequently accessed, in order to improve performance. Instead of querying
		the database for the same piece of information over and over again, the server should cache that piece of data, so as to save time
		and effort. 
		
	- Uniform Interface 
		* We should maintain a uniform, consistent, predictable way of interacting with our server. I.e. how URI's and HTTP methods are used
		should remain consistent, uniform, predictable, and ideally as convenient as possible. 
		
	- Client/Server relationship 
		* API should have envolving relationship with client that is using it. If a method is modified on one side, it should change behavior
		on the other. 
		
	- Layered Architecture 
		* Regardless of how complex our server or database may be, the client should be able to access our webservice as if it were monolithic. 
		Any complexity should be hidden from the client. 
	
	- Code on demand (optional)
		* The server should be able to send code to the client to run. 
		
10. What is Mockito?
	- Mockito is a package in java that essentially allows us to mock the output of certain methods. This allows us to test other methods in 
	isolation. In our project 0, it is primarily used to mock the outputs of our DAL layer when writing unit tests for our Service layer, however
	there is no reason that mockito couldn't be used to mock any other layer, or any other kind of method. 
	
11. What is the purpose of a mock object?
	- In order to provide an object that our system under test (SUT) requires. For example, our service layer in project 0 requires a Data 
	Layer Object in order to function. So we create a mock data access object to pass to our service layer constuctor. We may then mock any
	output that we care to from the mockDao object. 
	
12. How does mocking tie into the definition of a unit test?
	- Unit tests should test methods in isolation from other parts of our code. With methods that rely on other method to function, mocking 
	allows us to mock the behavior of these dependant functions to ensure that they will not be a point of failure, and that we are getting the 
	behavior that we want from them. This ensures that we are only testing the single method we want to test at that point. 
	- In sort, mocking allows us to spoof the isolation required for unit testing, even when there are methods depending on other methods. 
	
13. Why might we choose to use Javalin's exception mapping functionality over `try {} catch(... e) {}`?
	- Primarily, it provides a central location to catch any and all exceptions that may reach that point. If we catch all of our exceptions here, 
	it will allow us to have cleaner, simpler code with less redundency. Additionally, it may help us catch exceptions that we either forgot to
	catch, or that we couldn't catch for whatever reason within our handler functions. 
	
14. How does throwing exceptions in the service layer of our application help with implementing proper HTTP status codes?
	- If we throw exceptions from within our service layer, which is also the layer where we should be doing input validation, then we can also
	set a status code which better describes the issue encountered, if there was one. For example, we can throw a status code which indicats
	that the input provides was invalid, such as a name that is too long for our database. 
	
15. Why is logging important in an application?
	- Logging is important because it lets us keep track of relevant events, such as HTTP requests that have been sent, any errors encountered
	or other such relevant info. It allows us to have a record of events should anything ever go wrong for any reason. 
	
16. What are the 5 logging levels? What is the least important to most important?
	- Trace ***LEAST IMPORTANT***
	- Debug
	- Info
	- Warn
	- Error ***MOST IMPORTANT*** 
	
17. What is the purpose of an appender?
	- An appender allows us to configure what information is displayed/logged. For example, we can choose to only log Info and higher log events
	and not to log Debug and Trace. 
	
18. What is the ConsoleAppender and FileAppender?
	- ConsoleAppender is what allows us to configure what logging information is displayed in the console when we run our server. 
	- FileAppender is what allows us to configure what logging information is exported to our logfile when we run our server. 

</details>
