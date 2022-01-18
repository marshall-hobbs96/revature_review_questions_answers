# Java

1. What is a class?
	- A class is like a blueprint for objects. It allows one to define what fields an object will have when instantiated, what associated methods it will have, and the scopes for each.
	- There is a lot you can do to a class. Make it a singleton, javabean, follow a factory design pattern, etc. 
	
2. What is an object?
	- An Object is a specific instantiation, whose properties are defined by its associated class. This specific instantiation can then be manipulated. 
	
3. How is a class different than an object?
	- A class is the blueprint, an object is a real construct based off the blueprint. 
	
4. What are the four pillars of OOP?
	- Inheritence
	- Abstraction
	- Polymorphism
	- Encapsulation
	
5. What is inheritance?
	- Inheritance is the concept that child classes derived from parent classes *inherit* the properties of the parent class. 
	
6. What is encapsulation?
	- Encapsulation is the concept that all the required methods and properties that a class/object would need, is provided in the class definition. 
	- Even more basic, its the idea of *wrapping up* several related methods and fields into a single unit, so as to be provided in a single, cohensive package. 
	
7. What are the Java access modifiers and what do they each do?
	- Default, public, protected, private. 
	- Literally in the name. They modify who can access fields and methods within a class/instantiated object
	
8. What are getters/setters?
	- Methods dedicated to either setting the value of a field in a class/object, or getting the value of a field. 
	- Especially important because getter/setters allow one to create a class that follows the java bean design pattern.
	- In a java bean, fields are private, and so getter/setters are required to modify and access these fields. 
	
9. What is polymorphism?
	- Polymorphism is the idea that things can have different behaviors depending on different inputs or conditions. 
	- Method overriding and overloading is an example of polymorphism in action. 
	
10. Explain method overriding and overloading and how they are different from each other
	- Overriding: Changing the behavior of a method inherited from a parent class/interface
	- Overloading: Adding different parameters for a method that already exists within a class. In this way, the same method can accept different arguments, with different behaviors
	
11. What is abstraction?
	- Abstraction is the idea that we do not need to represent every small detail of something we want to represent in code. Instead, we can simple model its behavior. 
	- A good example would be a car. We need to model its important behaviors/properties, such as fuel capacity, speed, etc. 
	- However, we (likely) do not need to model every small detail of the car, such as the exact position/properties of fuel lines, air conditioning, etc. 
	- Therefore, we *abstract away* these smaller details in favor a simpler representation of the properties we are actually interest in. 
	
12. What are abstract methods?
	- Abstract methods are methods that cannot be actually called, but instead represent a method stub that needs to be actually implemented in classes that inherit it. 
	
13. What is an abstract class and how is it different from a regular class?
	- Abstract classes cannot be instantiated, and instead is intended to be inherited by other classes, in order to provide a basic frame for these inheriting classes. 

14. What is an interface?
	- An interface is very similar to an abstract class. However, by default, all methods MUST be implemented in the inheriting class. 
	
15. How many abstract classes can you extend? How many interfaces can you implement?
	- You can only extend one abstract class at a time. 
	- You can implement as many interfaces as you like at once.
	
16. Explain what Lists, Sets, and Maps are
	- These are different collections types. 
	- Lists: Ordered, can have copies of the same object within it
	- Sets: Unordered, cannot have copies
	- Maps: Maps a key to a value. Cannot have key copies, but values can repeat as much as you like
	
17. How is an Array different than a List?
	- An array has a fixed sized, while a list can expand and shrink.
	- Behind the scenes, it just creates new arrays im pretty sure
	
18. What is the difference between a List and Set?
	- List: Ordered, can have repeating values
	- Set: Unordered, cannot have repeating values
	
19. Can you access an element in a Set using an index? 
	- No
	
20. Are strings mutable or immutable?
	- Immutable. When you modify a string, you actually create a whole new string behind the scenes 
	
21. What is an exception?
	- An exception is an object used to help handle unintended or unexpected operation. 
	- For example, IllegalArgumentException is thrown whenever a method recieves invalid arguments
	- This exception is then (hopefully) caught, and exception handling behavior can be defined
	
22. Explain the difference between checked and unchecked exceptions
	- Checked: Checked at compile time. Therefore, will not let you compile if you do not catch or pass the buck on these exceptions
	- Unchecked: Its just not checked lol. If it happens it happens and if you dont handle it your program crashes lol
	
23. Explain throws v. throw
	- Throw: Create a new exception
	- Throws: Marks a method as capable of throwing exceptions that it wont handle itself 
	
24. What is try-with-resources?
	- This is a special try block that will automatically close any resources that are declared within the try block
	- For example, socket connections need to be closed when they are done being used. Try with resources provides the framework to achieve this
	
25. What is the purpose of the finally block?
	- Will always execute after a try/catch block, whether an exception is thrown or not
	
26. Can you have multiple catch blocks?
	- Yes, so long as they catch different exceptions

# SQL
1. What are the 5 sub-languages of SQL?
	- DDL: Data Definition Language
	- DML: Data Manipulation Language
	- DQL: Data Query Language
	- TCL: Transaction Query Language
	- DCL: Data Control Language
	
2. What commands are associated with DDL?
	- CREATE, ALTER, TRUNCATE, DROP
	
3. What commands are associated with DML?
	- INSERT, SELECT, UPDATE, DELETE
	
4. What commands are associated with DQL?
	- SELECT
	
5. What commands are associated with TCL?
	- COMMIT, ROLLBACK, SAVEPOINT
	
6. What commands are associated with DCL?
	- GRANT, REVOKE
	
7. What relationships can you have between tables? (multiplicity)
	- One to One
	- Many to One
	- One to Many
	- Many to Many
	
8. What SQL constraints are there?
	- Primary Key
	- Foreign Key
	- Not Null
	- Unique
	- Check (condition)
	- Default
	
9. What is the difference between LEFT/RIGHT, INNER, and OUTER joins?
	- 
10. What are scalar v. aggregate functions?

## SQL Query questions
1. Query for the employee from a table called Employee who has the highest salary
	- SELECT * FROM Employee WHERE (SELECT MAX(salary) FROM Employee)
	
2. Query for the employee from a table called Employee who has the SECOND highest salary
	- SELECT * FROM Employee WHERE(SELECT MAX(salary) FROM Employee WHERE Salary < (SELECT MAX(Salary) FROM Employee))
	
3. Join two tables together (what is the syntax for joining?)
	- SELECT * FROM Table1 JOIN Table2  
	
4. Given a table of Employee w/ the columns id, name, salary, and department, query for the average salary of each department (need to use GROUP BY and the AVG aggregate function)
	- 

# SDLC
1. What is the SDLC?
	- This is the Software Development Life Cycle. It is an ubiquitous outline of how software development should progress. 
	
2. What are the 7 phases of the SDLC?
	- Off the top of my head: Analysis, Planning, Development, Testing, Deployment, Maintenance 
	- Actual: Requirements, Analysis, Design, Development, Testing, Deployment, Maintenance 
	
3. Agile v. Waterfall?
	- Agile and Waterfall are both development philosophies for traversing the SDLC.
	- Waterfall advocates for going through each step in its entirety before moving onto the next step. No going back to previous steps. Deliver the entire project at once. 
	- Agile advocates for going throught he SDLC several times throughout the lifetime of a project, delivering small, functional bits of the overall project in consistent time periods. 
	
4. 4 Core values of Agile?
	- Off the top of my head: People over technologies, relationships over project mandates
	- Actual: Individuals and interactions over processes and tools, working software over comprehensive documentation, 
		Customer collaboration over contract negotiation, respoding to change over following a plan
		
5. Examples of Agile frameworks/methodologies?
	- Scrum is the big one
	- Kanban 
	- Xtreme programming
	
6. Explain Scrum in detail
	- Scrum is an implementation of the agile design philosophy....which in turn is a philosophy on the SDLC framework 
	- Includes several 'artifacts' to help guide development
		* Product backlog: a living document that includes all features intended to be developed within a project. Managed by the product owner
		* Sprint backlog: A semi living document that includes all features intended to be developed with a project FOR THE CURRENT SPRINT. Managed by the actual sprint development team/scrum master,
		with input from the product owner
		* Potentially releasable product increment: The result at the end of a sprint. Includes all the features that the development team worked on during the duration of the sprint that also
		matches the team definition of done. Represents the culmination of the Scrum/Agile design process. 
	- Includes several 'ceremonies' to help aid development 
		* Sprint planning meeting: Where the development team/scrum master/product owner discuss what features in the product backlog will be worked on during an upcoming sprint, as well as finer
		details about how the sprint will progress, who will work on what, etc. 
		* Daily Scrum: A daily, short meeting where everyone on the development team states what they worked on yesterday, what they plan on working on today, and what blockers/obstacles they may have
		* Sprint Review: A meeting at the end of a sprint where what was accomplished during the sprint is discussed, as well at the state of the potentially releasable product increment
		* Sprint Retrospective: A meeting after the sprint review, where the sprint and development process itself is reflected upon, so that improvements in the development process can be made
		
7. What is a Sprint?
	- A sprint is a block of time dedicated to the development of several features within a larger product. The idea is to traverse the majority of the SDLC for a small, specific subset
	of features within the larger product, so that these features can potentially be released before other parts of the product are done. In this way, the overall product is developed and potentially
	released in small, iterative pieces. 
	
8. What are the Scrum artifacts?
	- Product backlog, sprint backlog, potentially releasable product increment. 
	
9. What is a user story?
	- A user story is literally a story from the perspective of the user detailing how they would interact with a feature. For example, 'as a user, I want to be able to login using my username and password' 
	- Really, just a different/supplemental way to describe a feature
	
10. What is the product backlog? Who is in charge of managing the product backlog?
	- A living document that includes all features intended to be developed within a project. Managed by the product owner
	
11. What is the Sprint backlog? The user stories included in the Sprint backlog are decided in what Scrum meeting?
	- A semi living document that includes all features intended to be developed with a project FOR THE CURRENT SPRINT. Managed by the actual sprint development team/scrum master,
		with input from the product owner
12. What are acceptance criteria for a user story? How is this related to drafting test cases?
13. What Scrum roles are there?
14. Responsibilities of the Product Owner?
15. Responsibilities of the Scrum Master?
16. What Scrum ceremonies/meetings are there?
17. What questions should be answered during the daily standup meeting?
18. Sprint review v. Sprint retrospective meeting?
19. What are the 6 Scrum principles? https://www.scrumstudy.com/whyscrum/scrum-principles

# Testing Concepts
1. What is the mindset that a tester should have?
2. What are the phases in the testing lifecycle?
3. Verification v. Validation?
4. Activities involved with verification/static testing?
5. Validation testing is made up of what 2 subcategories?
6. What is functional testing?
7. What 4 types of tests make up the testing pyramid? What tradeoffs are there as you go from lower to higher in the pyramid?
8. What is whitebox v. blackbox testing?
9. Which tests are considered whitebox tests?
10. Which tests are considered blackbox tests?
11. What is the difference between positive and negative tests?
12. Should positive or negative tests be written first?
13. What is exploratory testing?
14. What is exhaustive testing and is it feasible?
15. Explain equivalence partitioning v. boundary testing
16. What is regression testing? Why is it important?
17. What is smoke testing? Why should smoke testing be done before regression testing?
18. What is sanity testing?
19. How does regression testing relate with DevOps and the process of deploying code to production?
20. What is manual testing? What type of formal structure/documents do we follow when executing tests manually?
21. What is test automation?
22. What tests are usually always automated? Which ones can be manual?
23. What is non-functional testing? What 2 subcategories are there?
24. What is performance testing?
25. Describe load, spike, ramp up/down and stress testing
26. What is usability testing?
27. What is a defect/bug?
28. What should happen when a defect is found by a tester?
29. Describe the defect lifecycle and the phases of the defect lifecycle
30. Describe what a defect report should contain
31. What severity and priority levels are there?
32. What is test driven development (TDD)?
33. What is behavior driven development (BDD)?

# Cucumber
1. What is a BDD framework?
2. Benefits of BDD?
3. Why use Cucumber + Selenium together w/ JUnit 5 instead of only Selenium + Cucumber?
4. What is Gherkin?
5. What type of file is Gherkin written inside of?
6. What three types of files do you need to deal with when writing BDD based tests?
7. What types of parameterization does Cucumber support?

# Selenium
1. What is Selenium?
2. What are the advantages of automation testing v. manual testing?
3. Selenium WebDriver v. Selenium IDE v. Selenium Grid? Which one did you use during training?
4. What are the steps to set up Selenium Java and navigate to a webpage?
5. How can we use the ChromeOptions object with the WebDriver object to open up an incognito browser?
6. What locators are there for Selenium?
7. Which locator is more efficient/faster: CSS or XPath locator?
8. Which locator is more flexible: CSS or XPath locator?
9. What is the difference between absolute v. relative XPath? Which one is more fragile?
10. `driver.findElement() v. driver.findElements()`?
11. What is the difference between implicit and explicit wait?
12. Why might we need to use waits?
13. `driver.close() v. driver.quit()`?
14. What method is used to click on an element?
15. What is method is used to type into an element?
16. What is the Actions class in Selenium? https://www.browserstack.com/guide/action-class-in-selenium

# DevOps
1. What is DevOps, and how is it related to Agile?
2. CI/CD: Continuous integration v. continuous delivery v. continuous deployment?
3. What is Jenkins?
4. What is a Jenkins pipeline?

# REST
1. What is REST?
2. By convention, what are the purposes of GET, POST, PUT, PATCH, DELETE?
3. How are resources represented in REST?
4. What are the REST URI conventions?
5. What are the 6 constraints of REST?
6. What are some of the best practices for REST API design?