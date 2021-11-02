# WEEK 3 REVIEW QUESTIONS
---
## DAY 1

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