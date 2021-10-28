# Question Practice Week 1

## Day 1
* What is Java?
	- Java is a modern programming language with an over 20 year history. According to [Wikipedia](https://en.wikipedia.org/wiki/Java_(programming_language)), 
"Java is a high-level, class-based, object-oriented programming language that is designed to have as few implementation dependencies as possible." Because Java had such
a long history, it has a mature developer community, meaning there are many projects and dependencies we can lean on when we're developing our own projects. 
* What are the benefits of Java?
	- High-level programming language
		* This means that Java is easier for humans to understand. High level programming languages allow us to code more efficiently by hiding the process of turning 
		it into machine code (or byte code, then machine code, in Java's case). Its easier to understand high level programming languages in contrast to low (or lower) level programming
		languages, such as the different types of [assembly languages](https://en.wikipedia.org/wiki/Assembly_language).
	- Object-oriented (Class-based)
		* Objected-oriented programming is the idea that all pieces of code should be associated with classes and objects. Everything in Java must be associated with a class. Even the main function is actually a part of a class. 
		This allows us to better organize and follow the 4 pillars of object oriented programming. 
	- Write once, run anywhere
		* One of the things that make Java truely stand out is that when you write and compile a Java program, you can then deploy it to any device that has the Java runtime enviroment installed on it.
* What is the difference between the JDK, JRE, and JVM?
	- JDK
		* JDK stands for Java development kit. In addition to the JRE and JVM, it also includes a compiler so that written Java code can be compiled into Java bytecode, which can then be executed on the JVM
	- JRE
		* JRE stands for Java runtime enviroment. This includes all the standard libraries included in java (java.lang package). The JRE is technically separate from the JVM, but they're always bundled together (JVM is a part of the JRE), as you 
		need both to run a java program (assuming its been compiled into java bytecode already). Classes like String are included in java.lang, which is part of the JRE
	- JVM	
		* JVM stands for Java Virtual Machine. This is the part of Java that actually runs the compiled java bytecode. See [Virtual Machines](https://en.wikipedia.org/wiki/Virtual_machine) if you wanna climb down that rabbithole.
* In order to run a Java program, what needs to happen first?
	- End user perspective 
		* Have the JRE installed on your computer along with the java program you want to run (should already be compiled and packaged for end users). Run the java program with the JRE.
	- Developer perspective	
		* Write the program. Compile and package it with JDK. Run it with JRE + JVM.  
* What is the significance of the main method?
	- The main method is the entrypoint for any program. It is what ties together any associated classes, packages, etc. If we think of our program as a car, the main method if the frame for the car that everything else goes in.
	If we want to get technical, the main method is the method that occupies the bottom of the stack. If you don't understand what that means, its fine for now. It will make more sense as you learn about what the stack is. [technically call stack] (https://en.wikipedia.org/wiki/Call_stack)
* What is an IDE?
	- IDE stands for integrated design enviroment. It is a program that allows for the programming, debugging, and running of programs within it. It is a very useful tool for development, because it automates what would otherwise
	be the tedious task of compiling, packaging, running and finding a way to debug a program ourselves. Aside from this, it also provides many other tools, such as project management tools. Overall, they (should) makes our lives easier.  
* What naming conventions does Java utilize?
	- Projects: snake case, nouns, undercase. Example: this-is-an-example
	- Packages: reverse domain name of company, then the package name. Example: com.revature.packagename
	- Classes: Camelcase, nouns, all first letters in a word capitalized. Example: ThisIsAClass
	- Methods: Camelcase, verbs, first word lowercase, capitalize first letter of each subsequent word. Example: thisIsAMethod
	- variables: CamelCase, nouns, first word lowercase, capitalize first letter of each subsequent word. Example: aVariable
* How can I write a Java application without an IDE such as Spring Tool Suite?
	- Easy. You just open a text editor and start typing. And hope you don't make any syntax errors. Should've asked how to compile and run it though....(javac on .java file. Java on the .class files. Good luck packaging it all)
* What is Bash?
	- A command line interface. More powerful alternative to the OS GUI, if you know how to use it. 
---

## Day 2
* What are classes in Java?
* What do classes contain?
* What are objects / instances of a class?
* What is the purpose of packages in Java?
* What is special about the java.lang package included in the Java runtime libraries?
* What are the primitive types in Java?
* Is String a primitive type?
* What are reference types?
* How are primitives and references different from each other?
* What does it mean when a reference type has a value of null?
* What makes an object eligible for garbage collection?
* What is garbage collection?
* What is a constructor and its purpose?
* What is constructor overloading?
* What is constructor chaining?
* What are the two uses of the `this` keyword?
* In terms of memory management, what is the stack and heap?
* What are methods?
* What are arguments v. parameters?
* What does method return type mean?
* What is the purpose of the `static` keyword?
* What can we use the `static` keyword with in Java?
* How can I access a static variable?
* How do I invoke a static method?
* What are instance variables?
* Can a static method access an instance variable directly?
* Can an instance method access an instance variable directly?
* What are the variable scopes in Java?
---

## Day 3
* What is Git?
* What is a local git repository?
* What is a remote git repository?
* What is the difference between Git and Github?
* What are some of the other popular repository hosting websites besides Github?
* What is the purpose of configuring the SSH keys for Github and Git Bash?
* Whenever we make changes to files or add/remove files from our local repository, what commands are needed to actually upload these changes to the remote repository?
* What arithmetic operators are there?
* What is numeric promotion?
* What are the assignment operators?
* What are the comparison operators?
* What are the logical operators?
* What does short-circuiting mean with the logical operators? Which are the short-circuiting operators?
* What two high level types of casting are there?
* Why does a narrowing conversion need to be explicit?
* Why does a widening conversion not need to be explicit?
* What is the difference between upcasting and downcasting?
* What is an example of downcasting?
* Why does downcasting need to be explicit?
* What datatypes can a switch statement use?
* What is the difference between a while loop and do-while loop?
* Write a for loop that prints numbers from 0 to 100 (inclusive), increasing
* Write a while loop that prints numbers from 500 to 250 (inclusive), decreasing
* Can arrays change in size?
* What is the syntax to instantiate an array?
* How are object arrays different than primitive arrays in memory?
* What is the for-each loop (enhanced for loop)?
---

## Day 4
* What is var-args?
* Can we have multiple var-args parameters for one method?
* Where does the var-args parameter need to go within the parameters?
* What type of variable is the var-args parameter, reference or primitive?
* What is the software development lifecycle?
* What are the 7 phases of the software development lifecycle?
* What two competing philosophies do we have?
* What is waterfall and its characteristics?
* What are the pros and cons of waterfall?
* When might we use waterfall?
* What is Agile?
* What are the core values of Agile?
* What are the 12 principles of Agile?
* What are some examples of Agile frameworks/methodologies?
* What is Scrum?
* What is a Sprint?
* What are the Scrum artifacts?
* What is a product backlog?
* Who is in charge of managing the product backlog?
* What is the Sprint backlog?
* How is it decided what items/user stories are included in the Sprint backlog?
* What is a usable product increment?
* What are user stories?
* What is "Acceptance Criteria"?
* What is the "Definition of Done"?
* What is "Story Pointing"?
* What is a burndown chart?
* What Scrum roles are there?
* What is the role of a Scrum Master?
* What is the role of the product owner?
* How large should a Scrum team be?
* What Scrum ceremonies are there?
* What questions should be answered by each team member during the daily standup meeting?
* What is the difference between the Sprint Review and Sprint Retrospective meeting?
* What is the purpose of the Java 8 Documentation? What is it actually documenting?
* What is the String pool?
* What are some common String methods?
* What is Maven?
* How do we include dependencies / external libraries into a Maven project?
* What is the purpose of the pom.xml file?
* What are the Maven project coordinates?
* What is Javalin?
* What are the three layers in three-tiered architecture?
* What is the purpose of the controller layer?
* What is the purpose of the service layer?
* What is the purpose of the data access layer?
---

## Day 5
* What three primary actions does a web browser perform?
* What is HTML?
* With regards to HTML, what is an attribute?
* What is the difference between HTML, CSS, and JavaScript?
* Where would we store our frontend files if we wanted to host them from our Javalin-based application?
* What is Selenium?
* How do we set up Selenium in order to go to Google.com?
* What Selenium locators do we have?
* What method in Selenium allows us to type text into an element?
* What method in Selenium allows us to click an element?