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
	- Classes are the basic building block in Java. Everything must be a part of a class. Classes are templates for instantiated objects. They contain
	variables and methods. 
* What do classes contain?
	- Variables and methods. There are any number of nuances associated with how these variables and methods can be accessed. 
* What are objects / instances of a class?
	- Objects / instances of a class are the same thing. They are just "real world" objects made from the "blueprint" of a class. For example, if you have a class
	named Dog, with several variables and methods, you can't really use it until you instantiate an object of the Dog class, such as fido. Ex: Dog fido = new Dog(); 
	- This ignores the idea of static variables and methods. That's a whole different concept. Lets ignore it for now. 
* What is the purpose of packages in Java?
	- The purpose of packages in Java is severalfold. First, it simply allows us to better organize our code. If we can separate groups of similar/related classes into
	packages, it can make our code easier to read, either for ourselves going back, or to other developers using our code. 
	- Secondly, it makes our code more portable. If we have all of our classes for a program in one package, it makes it less convenient if we want to use just a few of 
	the classes inside it. We would have to import the entire package, and therefore have extra classes we wouldn't be using. Better to seperate out related classes into their
	own packages, that way in the future if we need to use them, we can just import a smaller, more managable package. 
	- Lastly, it offers a bit of abstraction (which is one of four pillars of OOP or object oriented programming). For example, if we have two different packages we want to import
	into our project, they can share class names within each package without there being too much trouble. You'll still run into a bit of trouble, but its possible to use the same
	class name from two different packages. 
* What is special about the java.lang package included in the Java runtime libraries?
	- The java.lang package is special because it never needs to be imported. It is always imported into Java programs automatically. It includes many usefull classes
	such as String
* What are the primitive types in Java?
	- There are 8 primitive data types in Java: boolean, byte, char, int, short, long, float, and double
* Is String a primitive type?
	- String is not a primitive type. It is a class that is included in the java.lang package. 
* What are reference types?
	- Reference types are variables for anything other than a primitive. This is because if a variable is not a primitive, it must necessarily be a class type(reference) variable. 
	Reference variables point to the location of objects in memory, specifically memory locations in the heap. 
* How are primitives and references different from each other?
	- Primitives directly store a value, and are located within the stack in memory. References point to the location in memory on the heap where the object is. 
* What does it mean when a reference type has a value of null?
	- If a reference type has a value of null, that means it currently does not point to any location in memory, and therefore has no object associated with it. 
* What makes an object eligible for garbage collection?
	- An object is eligible for garbage collection if there are no more reference variables pointing to it. 
* What is garbage collection?
	- Garbage collection is the automatic deallocation of memory associated with objects with no more reference to them. This is to prevent memory leaks. It also
	makes java a bit easier to program, because developers don't need to worry about manual memory management. 
* What is a constructor and its purpose?
	- A constructor is a method associated with a class. Its used to initialize the properties of an object of that class type. Constructor methods have the same name
	as the class it is a constructor for. 
* What is constructor overloading?
	- Constructor overloading is the process of creating multiple different constructors with different types and/or number of parameters. This allows us flexibility in 
	how we initialize objects of a class. 
* What is constructor chaining?
	- Constructor chaining is the process of using one constructor of a class in another. This primarily serves to make our code cleaner and more organized. We could write
	several different constructors that build on each other, and we could just copy paste the code from the simpler constructors into the more complex ones. Or we could just
	call the simpler constructors inside the more complex ones, and then add on whatever additional functionality we want. 
* What are the two uses of the `this` keyword?
	- The `this` keyword is used for referencing the current object. Thats really its only use. I suppose you could use it in constructors to references the object being constructed
	and you could use it in methods as well to reference the current object calling the method, but thats really the same thing. Your just referencing the current object. 
* In terms of memory management, what is the stack and heap?
	- The stack is where method information is stored. This includes data like variables. The heap is where objects are stored. 
* What are methods?
	- Methods are chunks of code associated with classes and/or objects that perform certain functions. 
* What are arguments v. parameters?
	- Parameters are what you use when you write methods. They are stand ins for what you will eventually pass to the method when you use it.
	Arguments are what you actually pass to the method when you use it. 
* What does method return type mean?
	- Method return type is the type of of what the method will return when it finishes. For example, when a method return type is int, it will return an int type when it completes. 
* What is the purpose of the `static` keyword?
	- The static keyword is used to denote a variable or method as belonging to the class itself, as opposed to belonging to any individual objects. 
* What can we use the `static` keyword with in Java?
	- We can use the static keyword with any variables or methods in a class. 
* How can I access a static variable?
	- You can access a static variable from the class name itself, or from any object of that class. 
* How do I invoke a static method?
	- You can invoke a static method either from the classname itself, or from any object of that class. 
* What are instance variables?
	- Instance variables are variables that belong to an object, as opposed to the class. 
* Can a static method access an instance variable directly?
	- No
* Can an instance method access an instance variable directly?
	- Yes
* What are the variable scopes in Java?
	- Class (static) scope. 
	- Method scope
	- Instance scope
	- Block scope 
---

## Day 3
* What is Git?
	- Git is a version control software. Its a powerful tool for maintaining software, especially in collaborative enviroments. 
* What is a local git repository?
	- A local git repository is a local storage of code. I.e. a place where you've stored code on your own computer, and are running git inside of. Can be linked to a remote repository 
* What is a remote git repository?
	- A remote git repository is a remote storeage of code. Github is a popular place to host remote git repositories. 
* What is the difference between Git and Github?
	- Git is a version control software. Github is a place for (mostly) hosting remote git repositories. 
* What are some of the other popular repository hosting websites besides Github?
	- Gitlab is one I think. Are they really even relevant? 
* What is the purpose of configuring the SSH keys for Github and Git Bash?
	- So that git/github can verify your identity. Github especially doesn't like anonymous people pushing to repositories. 
* Whenever we make changes to files or add/remove files from our local repository, what commands are needed to actually upload these changes to the remote repository?
	- git init (initialize local git repository) 
	- git add filename (or just `.` instead of file name, if you want to add all the files in the current directory)
	- git commit -m "message for the commit" 
	- git push origin main (assuming you've already set that up) 
* What arithmetic operators are there?
	- +, -, *, /, % 
* What is numeric promotion?
	- The automatic casting of one, smaller numeric type, to another larger one. For example, float i = 2; i is a float, but 2 is an int type. So 2 is automatically
	cast to a float type or "promoted" to a float type. 
* What are the assignment operators?
	- really theres just `=`. Every other assignment operator is really just a short hand combination, such as `+=`, `-=`, etc. 
* What are the comparison operators?
	- ==, != , <, >, >=, <=
* What are the logical operators?
	- !, &, &&, |, ||
* What does short-circuiting mean with the logical operators? Which are the short-circuiting operators?
	- Short circuiting means that, if the lefthand side of the logical comparison is determinate, it wont evaluate the right hand side. 
	- For example, if we have true || false, this wont even evaluate the right hand side, because the left hand side will always make || (or) true. 
	- || and  && are the short circuiting versions of `or` and `and`
* What two high level types of casting are there?
	- Downcasting (casting a parent class type to a child type variable, dangerous)
	- upcasting (casting a child class type to a parent type variable)
* Why does a narrowing conversion need to be explicit?
	- Narrowing needs to be explicit because, for example, if we go from a 64 bit numeric to a 32 bit numeric type, then we will necessarily loose some data. 
	If that data is empty, then its fine, but if that data was being used to store the value, then the value of our variable will change when we narrow it. 
	This is why narrowing is dangerous, because it has the potential to change the value of our variables without us intending it. 
* Why does a widening conversion not need to be explicit?
	- Because going from a 32 bit datatype to a 64 bit datatype wont destroy any data, only create it. 
* What is the difference between upcasting and downcasting?
	- Downcasting (casting a parent class type to a child type variable, dangerous)
	- upcasting (casting a child class type to a parent type variable)
* What is an example of downcasting?
	- If we have two classes, one called Parent and one called Child, and Child is a child class of Parent. Then an example of downcasting would be...
	Child child = new (Child)Parent(); 
* Why does downcasting need to be explicit?
	- Downcasting needs to be explicit because it can be dangerous. 
	- It can be dangerous because child classes generally have additional datamembers that parent classes do not. This can cause many problems. 
* What datatypes can a switch statement use?
	- byte, int, short, String, enum 
* What is the difference between a while loop and do-while loop?
	- a do-while loop will always execute once before checking the loop condition. A regular while loop will always check the condition first before starting the loop. 
* Write a for loop that prints numbers from 0 to 100 (inclusive), increasing
	- for(int i = 0; i<= 100; i++) {
	
		System.out.print(i + " "); 
	
	}
* Write a while loop that prints numbers from 500 to 250 (inclusive), decreasing
	- int i = 500; 
	while(i >= 250) {
	
		System.out.print(i + " "); 
		i--; 
	
	}
* Can arrays change in size?
	- No, they are fixed size 
* What is the syntax to instantiate an array?
	- int[] array = new int[5]; << = the `5` can be any number you want really 
* How are object arrays different than primitive arrays in memory?
	- Primitive arrays have an array with the actual primitive values stored in it. Reference arrays have arrays of references stored in it that point to the actual objects. 
* What is the for-each loop (enhanced for loop)?
	- the enhanced for loop is a shortcut that allows one to write a for loop that will iterate over all elements of a type in a collection. 
---

## Day 4
* What is var-args?
	- var-args a parameter we can specifiy in a method that allows us to have a variable number of arguments. Useful for when we want a method that can accept
	large number of arguments of a certain type. 
* Can we have multiple var-args parameters for one method?
	- No, we can only have one var-args parameter for a method. This is because if we have multiple var-arg parameters, the method/compiler won't know when the arguments
	for one var-args ends and the other ends 
* Where does the var-args parameter need to go within the parameters?
	- The var-args should always go at the end of the parameters list. Again, this is to prevent the method/compiler getting confused about where the var-args
	list ends, and the other parameters begins. 
* What type of variable is the var-args parameter, reference or primitive?
	- It is a reference parameter. This is because var-args are necessarily an array type. Array variables are reference variables. 
* What is the software development lifecycle?
	- The software development cycle is the steps/phases neccesary for describing the complete life cycle of a specific application or feature. 
* What are the 7 phases of the software development lifecycle?
	- Requirments phase 
		* What needs to be developed? Very conceptual. 
	- Analysis Phase 
		* Gathering together technical documents. Ironing out requirments and getting more specific/concrete about what it is we're going to make. 
		* Software Requirment Specification (SRS) document made. Formally defines software and hardware requirments. 
	- Design Phase 
		* Getting even more into the weeds of what were going to design. More design documents made. Psuedocode written. Outline of technical details 
	- Development Phase 
		* This is where all the code is actually written. No more planning, just getting it done. 
	- Testing Phase 
		* Formal testing occurs here to make sure it meets all requirments set out in the design phase.
	- Deployment Phase 
		* Code is actually deployed for use. Can be used by clients/customers/end users at this point 
	- Maintainence Phase 
		* Just making sure it continues to run at this point. Solving bugs, ironing out any quirks or missed details. Patches. 
* What two competing philosophies do we have?
	- Waterfall and Agile
* What is waterfall and its characteristics?
	- Waterfall is a development philosophy for going through the steps of the software development life cycle (SDLC). It essentially focuses on completeing one step 
	at a time of the SDLC fully, then moving onto the next. It doesn't allow going back to previous steps. 
* What are the pros and cons of waterfall?
	- Pros
		* Good for large organizations where many people are working on a single project at once	
		* Good when the project requirments will not change after the planning phase 
		* Good for when you need all your deliverables deployed at once, as opposed to incrementally deployed
	- Cons 
		* Not as effective when you have smaller groups/smaller projects
		* Doesn't allow for going back to previous steps in SDLC, so terrible for projects where requirments might change or change frequently 
		* Terrible for when a project needs small, iterative development/deployment
* When might we use waterfall?
	- Waterfall would benefit from highly regulated and/or government work 
* What is Agile?
	- Agile is a competing development philosohphy to waterfall. It essentially allows for going through the SDLC many times, in order to complete smaller
	parts of the overall project one at a time. 
* What are the core values of Agile?
	- Individuals and interactions over processes and tools 
	- Working software over comprehensive documentation 
	- Customer collaboration over contract negotiation 
	- Responding to change over following a plan 
* What are the 12 principles of Agile?
	- I think its kind of excessive to remember all 12 of these from memory, so I'm just going to copy past these from the recap notes. 
	- The highest priority is to satisfy the customer through early and **continuous delivery** of valuable software
	- Deliver working software frequently, from a couple of weeks to a couple of months, with a preference to the shorter timescale
	- Working software is the primary measure of progress
	- Agile processes promote sustainable development. The sponsors, developers, and users should be able to maintain a constant pace indefinitely
	- Business people and developers MUST work together daily throughout the project
	- The most efficient and effective method of conveying information to and within a development team is face-to-face conversation
	- The best architectures, requirements, and designs emerge from self-organizing teams
	- Build projects around motivated individuals. Give them the environment and support they need and trust them to get the job done.
	- At regular intervals, the team reflects on how to become more effective, then tunes and adjusts their behavior accordingly
	- Continuous attention to technical excellence and good design enhances agility
	- Simplicity, the art of maximizing the amount of work NOT done, is essential
	- Agile processes harness change for the customer's competitive advantage
* What are some examples of Agile frameworks/methodologies?
	- Scrum 
	- Kanban 
	- Extreme Programming (XP) 
* What is Scrum?
	- Scrum is a concrete implementation of the agile development philosophy. Its describes actionable steps and processes to follow in order to 
	implement the agile development philosophy. 
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