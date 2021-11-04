# Question Practice Week 1

## Day 1

<details> 

<summary> Click to expand </summary> 

1. What is Java?
	- Java is a modern programming language with an over 20 year history. According to [Wikipedia](https://en.wikipedia.org/wiki/Java_(programming_language)), 
"Java is a high-level, class-based, object-oriented programming language that is designed to have as few implementation dependencies as possible." Because Java had such
a long history, it has a mature developer community, meaning there are many projects and dependencies we can lean on when we're developing our own projects. 

2. What are the benefits of Java?
	- High-level programming language
		* This means that Java is easier for humans to understand. High level programming languages allow us to code more efficiently by hiding the process of turning 
		it into machine code (or byte code, then machine code, in Java's case). Its easier to understand high level programming languages in contrast to low (or lower) level programming
		languages, such as the different types of [assembly languages](https://en.wikipedia.org/wiki/Assembly_language).
	- Object-oriented (Class-based)
		* Objected-oriented programming is the idea that all pieces of code should be associated with classes and objects. Everything in Java must be associated with a class. Even the main function is actually a part of a class. 
		This allows us to better organize and follow the 4 pillars of object oriented programming. 
	- Write once, run anywhere
		* One of the things that make Java truely stand out is that when you write and compile a Java program, you can then deploy it to any device that has the Java runtime enviroment installed on it.

3. What is the difference between the JDK, JRE, and JVM?
	- JDK
		* JDK stands for Java development kit. In addition to the JRE and JVM, it also includes a compiler so that written Java code can be compiled into Java bytecode, which can then be executed on the JVM
	- JRE
		* JRE stands for Java runtime enviroment. This includes all the standard libraries included in java (java.lang package). The JRE is technically separate from the JVM, but they're always bundled together (JVM is a part of the JRE), as you 
		need both to run a java program (assuming its been compiled into java bytecode already). Classes like String are included in java.lang, which is part of the JRE
	- JVM	
		* JVM stands for Java Virtual Machine. This is the part of Java that actually runs the compiled java bytecode. See [Virtual Machines](https://en.wikipedia.org/wiki/Virtual_machine) if you wanna climb down that rabbithole.

4. In order to run a Java program, what needs to happen first?
	- End user perspective 
		* Have the JRE installed on your computer along with the java program you want to run (should already be compiled and packaged for end users). Run the java program with the JRE.
	- Developer perspective	
		* Write the program. Compile and package it with JDK. Run it with JRE + JVM.  

5. What is the significance of the main method?
	- The main method is the entrypoint for any program. It is what ties together any associated classes, packages, etc. If we think of our program as a car, the main method if the frame for the car that everything else goes in.
	If we want to get technical, the main method is the method that occupies the bottom of the stack. If you don't understand what that means, its fine for now. It will make more sense as you learn about what the stack is. [technically call stack] (https://en.wikipedia.org/wiki/Call_stack)

6. What is an IDE?
	- IDE stands for integrated design enviroment. It is a program that allows for the programming, debugging, and running of programs within it. It is a very useful tool for development, because it automates what would otherwise
	be the tedious task of compiling, packaging, running and finding a way to debug a program ourselves. Aside from this, it also provides many other tools, such as project management tools. Overall, they (should) makes our lives easier.  

7. What naming conventions does Java utilize?
	- Projects: snake case, nouns, undercase. Example: this-is-an-example
	- Packages: reverse domain name of company, then the package name. Example: com.revature.packagename
	- Classes: Camelcase, nouns, all first letters in a word capitalized. Example: ThisIsAClass
	- Methods: Camelcase, verbs, first word lowercase, capitalize first letter of each subsequent word. Example: thisIsAMethod
	- variables: CamelCase, nouns, first word lowercase, capitalize first letter of each subsequent word. Example: aVariable

8. How can I write a Java application without an IDE such as Spring Tool Suite?
	- Easy. You just open a text editor and start typing. And hope you don't make any syntax errors. Should've asked how to compile and run it though....(javac on .java file. Java on the .class files. Good luck packaging it all)

9. What is Bash?
	- A command line interface. More powerful alternative to the OS GUI, if you know how to use it. 

</details>

---

## Day 2

<details>

<summary> click to expand </summary> 

1. What are classes in Java?
	- Classes are the basic building block in Java. Everything must be a part of a class. Classes are templates for instantiated objects. They contain
	variables and methods. 

2. What do classes contain?
	- Variables and methods. There are any number of nuances associated with how these variables and methods can be accessed. 

3. What are objects / instances of a class?
	- Objects / instances of a class are the same thing. They are just "real world" objects made from the "blueprint" of a class. For example, if you have a class
	named Dog, with several variables and methods, you can't really use it until you instantiate an object of the Dog class, such as fido. Ex: Dog fido = new Dog(); 
	- This ignores the idea of static variables and methods. That's a whole different concept. Lets ignore it for now. 

4. What is the purpose of packages in Java?
	- The purpose of packages in Java is severalfold. First, it simply allows us to better organize our code. If we can separate groups of similar/related classes into
	packages, it can make our code easier to read, either for ourselves going back, or to other developers using our code. 
	- Secondly, it makes our code more portable. If we have all of our classes for a program in one package, it makes it less convenient if we want to use just a few of 
	the classes inside it. We would have to import the entire package, and therefore have extra classes we wouldn't be using. Better to seperate out related classes into their
	own packages, that way in the future if we need to use them, we can just import a smaller, more managable package. 
	- Lastly, it offers a bit of abstraction (which is one of four pillars of OOP or object oriented programming). For example, if we have two different packages we want to import
	into our project, they can share class names within each package without there being too much trouble. You'll still run into a bit of trouble, but its possible to use the same
	class name from two different packages. 

5. What is special about the java.lang package included in the Java runtime libraries?
	- The java.lang package is special because it never needs to be imported. It is always imported into Java programs automatically. It includes many usefull classes
	such as String

6. What are the primitive types in Java?
	- There are 8 primitive data types in Java: boolean, byte, char, int, short, long, float, and double

7. Is String a primitive type?
	- String is not a primitive type. It is a class that is included in the java.lang package. 

8. What are reference types?
	- Reference types are variables for anything other than a primitive. This is because if a variable is not a primitive, it must necessarily be a class type(reference) variable. 
	Reference variables point to the location of objects in memory, specifically memory locations in the heap. 

9 How are primitives and references different from each other?
	- Primitives directly store a value, and are located within the stack in memory. References point to the location in memory on the heap where the object is. 

10. What does it mean when a reference type has a value of null?
	- If a reference type has a value of null, that means it currently does not point to any location in memory, and therefore has no object associated with it. 

11. What makes an object eligible for garbage collection?
	- An object is eligible for garbage collection if there are no more reference variables pointing to it. 

12. What is garbage collection?
	- Garbage collection is the automatic deallocation of memory associated with objects with no more reference to them. This is to prevent memory leaks. It also
	makes java a bit easier to program, because developers don't need to worry about manual memory management. 

13. What is a constructor and its purpose?
	- A constructor is a method associated with a class. Its used to initialize the properties of an object of that class type. Constructor methods have the same name
	as the class it is a constructor for. 

14. What is constructor overloading?
	- Constructor overloading is the process of creating multiple different constructors with different types and/or number of parameters. This allows us flexibility in 
	how we initialize objects of a class. 

15. What is constructor chaining?
	- Constructor chaining is the process of using one constructor of a class in another. This primarily serves to make our code cleaner and more organized. We could write
	several different constructors that build on each other, and we could just copy paste the code from the simpler constructors into the more complex ones. Or we could just
	call the simpler constructors inside the more complex ones, and then add on whatever additional functionality we want. 

16. What are the two uses of the `this` keyword?
	- The `this` keyword is used for referencing the current object. Thats really its only use. I suppose you could use it in constructors to references the object being constructed
	and you could use it in methods as well to reference the current object calling the method, but thats really the same thing. Your just referencing the current object. 

17. In terms of memory management, what is the stack and heap?
	- The stack is where method information is stored. This includes data like variables. The heap is where objects are stored. 

18. What are methods?
	- Methods are chunks of code associated with classes and/or objects that perform certain functions. 

19. What are arguments v. parameters?
	- Parameters are what you use when you write methods. They are stand ins for what you will eventually pass to the method when you use it.
	Arguments are what you actually pass to the method when you use it. 

20. What does method return type mean?
	- Method return type is the type of of what the method will return when it finishes. For example, when a method return type is int, it will return an int type when it completes. 

21. What is the purpose of the `static` keyword?
	- The static keyword is used to denote a variable or method as belonging to the class itself, as opposed to belonging to any individual objects. 

22. What can we use the `static` keyword with in Java?
	- We can use the static keyword with any variables or methods in a class. 

23. How can I access a static variable?
	- You can access a static variable from the class name itself, or from any object of that class. 

24. How do I invoke a static method?
	- You can invoke a static method either from the classname itself, or from any object of that class. 

25. What are instance variables?
	- Instance variables are variables that belong to an object, as opposed to the class. 

26. Can a static method access an instance variable directly?
	- No

27. Can an instance method access an instance variable directly?
	- Yes

28. What are the variable scopes in Java?
	- Class (static) scope. 
	- Method scope
	- Instance scope
	- Block scope 
	
</details> 
	
---

## Day 3

<details> 

<summary> Click to expand </summary>

1. What is Git?
	- Git is a version control software. Its a powerful tool for maintaining software, especially in collaborative enviroments. 

2. What is a local git repository?
	- A local git repository is a local storage of code. I.e. a place where you've stored code on your own computer, and are running git inside of. Can be linked to a remote repository 
 What is a remote git repository?
	- A remote git repository is a remote storeage of code. Github is a popular place to host remote git repositories. 

3. What is the difference between Git and Github?
	- Git is a version control software. Github is a place for (mostly) hosting remote git repositories. 

4. What are some of the other popular repository hosting websites besides Github?
	- Gitlab is one I think. Are they really even relevant? 

5. What is the purpose of configuring the SSH keys for Github and Git Bash?
	- So that git/github can verify your identity. Github especially doesn't like anonymous people pushing to repositories. 

6. Whenever we make changes to files or add/remove files from our local repository, what commands are needed to actually upload these changes to the remote repository?
	- git init (initialize local git repository) 
	- git add filename (or just `.` instead of file name, if you want to add all the files in the current directory)
	- git commit -m "message for the commit" 
	- git push origin main (assuming you've already set that up) 

7. What arithmetic operators are there?
	- +, -, *, /, % 

8. What is numeric promotion?
	- The automatic casting of one, smaller numeric type, to another larger one. For example, float i = 2; i is a float, but 2 is an int type. So 2 is automatically
	cast to a float type or "promoted" to a float type. 

9. What are the assignment operators?
	- really theres just `=`. Every other assignment operator is really just a short hand combination, such as `+=`, `-=`, etc. 

10. What are the comparison operators?
	- ==, != , <, >, >=, <=

11. What are the logical operators?
	- !, &, &&, |, ||

12. What does short-circuiting mean with the logical operators? Which are the short-circuiting operators?
	- Short circuiting means that, if the lefthand side of the logical comparison is determinate, it wont evaluate the right hand side. 
	- For example, if we have true || false, this wont even evaluate the right hand side, because the left hand side will always make || (or) true. 
	- || and  && are the short circuiting versions of `or` and `and`

13. What two high level types of casting are there?
	- Downcasting (casting a parent class type to a child type variable, dangerous)
	- upcasting (casting a child class type to a parent type variable)

14. Why does a narrowing conversion need to be explicit?
	- Narrowing needs to be explicit because, for example, if we go from a 64 bit numeric to a 32 bit numeric type, then we will necessarily loose some data. 
	If that data is empty, then its fine, but if that data was being used to store the value, then the value of our variable will change when we narrow it. 
	This is why narrowing is dangerous, because it has the potential to change the value of our variables without us intending it. 

15. Why does a widening conversion not need to be explicit?
	- Because going from a 32 bit datatype to a 64 bit datatype wont destroy any data, only create it. 

16. What is the difference between upcasting and downcasting?
	- Downcasting (casting a parent class type to a child type variable, dangerous)
	- upcasting (casting a child class type to a parent type variable)

17. What is an example of downcasting?
	- If we have two classes, one called Parent and one called Child, and Child is a child class of Parent. Then an example of downcasting would be...
	Child child = new (Child)Parent(); 

18. Why does downcasting need to be explicit?
	- Downcasting needs to be explicit because it can be dangerous. 
	- It can be dangerous because child classes generally have additional datamembers that parent classes do not. This can cause many problems. 

19. What datatypes can a switch statement use?
	- byte, int, short, String, enum 

20. What is the difference between a while loop and do-while loop?
	- a do-while loop will always execute once before checking the loop condition. A regular while loop will always check the condition first before starting the loop. 

21. Write a for loop that prints numbers from 0 to 100 (inclusive), increasing
	- for(int i = 0; i<= 100; i++) {
	
		System.out.print(i + " "); 
	
	}

22. Write a while loop that prints numbers from 500 to 250 (inclusive), decreasing
	- int i = 500; 
	while(i >= 250) {
	
		System.out.print(i + " "); 
		i--; 
	
	}

23. Can arrays change in size?
	- No, they are fixed size 

24. What is the syntax to instantiate an array?
	- int[] array = new int[5]; << = the `5` can be any number you want really 

25. How are object arrays different than primitive arrays in memory?
	- Primitive arrays have an array with the actual primitive values stored in it. Reference arrays have arrays of references stored in it that point to the actual objects. 

26. What is the for-each loop (enhanced for loop)?
	- the enhanced for loop is a shortcut that allows one to write a for loop that will iterate over all elements of a type in a collection. 

</details> 

---

## Day 4

<details> 
<summary> Click to expand </summary>

1. What is var-args?
	- var-args a parameter we can specifiy in a method that allows us to have a variable number of arguments. Useful for when we want a method that can accept
	large number of arguments of a certain type. 

2. Can we have multiple var-args parameters for one method?
	- No, we can only have one var-args parameter for a method. This is because if we have multiple var-arg parameters, the method/compiler won't know when the arguments
	for one var-args ends and the other ends 

3. Where does the var-args parameter need to go within the parameters?
	- The var-args should always go at the end of the parameters list. Again, this is to prevent the method/compiler getting confused about where the var-args
	list ends, and the other parameters begins. 

4. What type of variable is the var-args parameter, reference or primitive?
	- It is a reference parameter. This is because var-args are necessarily an array type. Array variables are reference variables. 

5. What is the software development lifecycle?
	- The software development cycle is the steps/phases neccesary for describing the complete life cycle of a specific application or feature. 

6. What are the 7 phases of the software development lifecycle?
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

7. What two competing philosophies do we have?
	- Waterfall and Agile

8. What is waterfall and its characteristics?
	- Waterfall is a development philosophy for going through the steps of the software development life cycle (SDLC). It essentially focuses on completeing one step 
	at a time of the SDLC fully, then moving onto the next. It doesn't allow going back to previous steps. 

9. What are the pros and cons of waterfall?
	- Pros
		* Good for large organizations where many people are working on a single project at once	
		* Good when the project requirments will not change after the planning phase 
		* Good for when you need all your deliverables deployed at once, as opposed to incrementally deployed
	- Cons 
		* Not as effective when you have smaller groups/smaller projects
		* Doesn't allow for going back to previous steps in SDLC, so terrible for projects where requirments might change or change frequently 
		* Terrible for when a project needs small, iterative development/deployment

10. When might we use waterfall?
	- Waterfall would benefit from highly regulated and/or government work 

11. What is Agile?
	- Agile is a competing development philosohphy to waterfall. It essentially allows for going through the SDLC many times, in order to complete smaller
	parts of the overall project one at a time. 

12. What are the core values of Agile?
	- Individuals and interactions over processes and tools 
	- Working software over comprehensive documentation 
	- Customer collaboration over contract negotiation 
	- Responding to change over following a plan 

13. What are the 12 principles of Agile?
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

14. What are some examples of Agile frameworks/methodologies?
	- Scrum 
	- Kanban 
	- Extreme Programming (XP) 

15. What is Scrum?
	- Scrum is a concrete implementation of the agile development philosophy. Its describes actionable steps and processes to follow in order to 
	implement the agile development philosophy. 

16. What is a Sprint?
	- A sprint is essentially a self contained iteration through the SDLC for a subfeature or set of subfeatures of the overall project. Its intended to 
	allow a development group to be able to completely deploy working code for a piece of the overall project at the end of the sprint. Sprints typically 
	last anywhere from 1 to 3 weeks. 

17. What are the Scrum artifacts?
	- Scrum artifacts are documents to assist in the scrum development process. They provide a framework, reference, and anchor for developers to use in order 
	to remain on task during a sprint. They allows developers to know what they need to work on, and the criteria to know if they've actually completed it. 

18. What is a product backlog?
	- The product backlog is a list of features that needs to be completed for the project. Ideally, it is constantly changing and having new features added
	to it. 

19. Who is in charge of managing the product backlog?
	- The "product owner", which is typically just a project manager

20. What is the Sprint backlog?
	- A sprint backlog is a document that contains all of the features that need to be worked on/implemented during a sprint. Once a sprint starts, only the development
	team can add items. However, they must negotiate with the product owner to remove items. 

21. How is it decided what items/user stories are included in the Sprint backlog?
	- Its typically decided by the product owner and the scrum master, potentially with input from the rest of the development team. Its typically decided by what is believed can 
	be accomplished by the development team during a sprint. It also includes features from previous sprints that may not have been fully completed. 

22. What is a usable product increment?
	- This is what you have at the end of the sprint. It is essentially a completed feature or set of features that would ***ideally*** be deployable. 

23. What are user stories?
	- User stories are descriptions of features of a project from the perspective of the end-user. These are the way that the features to be implemented in the product 
	and sprint backlog are described. 

24. What is "Acceptance Criteria"?
	- Acceptance criteria is a description of what would make a feature that is being developed "done" from the perspective of the user. Essentially it asks, can this 
	feature let a user do x, y, and z? If so, then we can consider that feature complete. 

25. What is the "Definition of Done"?
	- The "Definition of Done" is how a scrum team determines if a feature is truly completed. It generally includes passing the acceptance criteria, along with other criteria
	such as passing testing and/or quality assurance. 

26. What is "Story Pointing"?
	- Story pointing is assigning a difficulty value of some kind to describe how hard it would be to complete a certain user story. In contrast to simply saying "I think this
	will take 2 weeks to complete" you would say something like, "This an avengers level threat". Actually thats probably a bad example. It would be better to give it levels, 
	like this is a level 40 monster (user story) to describe something that is fairly difficult, or a level 5 monster (user story) if its fairly trivial. 

27. What is a burndown chart?
	- A burndown chart is just a chart that allows the scrum team to visually represent the progress being made on a sprint backlog visually. Its graphs the number of user stories
	left to complete on the y axis, and time on the x axis. 

28. What Scrum roles are there?
	- Scrum master 
		* person that is responsible for leading the team through the scrum process. Essentially a team lead that makes sure the scrum process is being followed appropriatly. 
	- Product owner 
		* Person who is responsible for deciding what features are to be listed in the product backlog. Essentially a project lead. Serves as point of contact between dev team and client
	- Development team 
		* people who are responsible for actually writing the code and what not. 

29. What is the role of a Scrum Master?
	- Oversee the scrum process. Help maintain sprint backlog. 

30. What is the role of the product owner?
	- Serve as point of contact between client and dev team. Maintain product backlog

31. How large should a Scrum team be?
	- No bigger than 10 people

32. What Scrum ceremonies are there?
	- Sprint planning meeting
	- Daily standup meeting 
	- Sprint review meeting 
	- Sprint retrospective 

33. What questions should be answered by each team member during the daily standup meeting?
	- What did you do yesterday? 
	- What will you do today? 
	- What issues/blockers have you run into? 

34. What is the difference between the Sprint Review and Sprint Retrospective meeting?
	- The sprint review is more for reviewing the outcome of the sprint, while the retrospective is more for analyzing what could be improved for the next sprint.

35. What is the purpose of the Java 8 Documentation? What is it actually documenting?
	- The purpose of the Java 8 Documentation is to provide information on all the different classes, their data members, associated methods, and how they are intended
	to be used. It is to help developers more effectivly use and understand the java standard library. 

36. What is the String pool?
	- The string pool is a special part of the heap where String literals that have been instantiated are stored. Its intented to help save memory. It does this by 
	limiting each unique String to having one String object in the String Pool. For example, if you has String a = "Hello"; and String b = "Hello", both `a` and `b` would
	point to the same String object "Hello" in the String Pool, saving a bit of memory. String objects instantiated with the new keyword, as in String c = new String(), are
	kept in the regular part of the heap, so you can have several String objects with the same value this way. 

37. What are some common String methods?
	- .concat(String s); .length(); .charAt(int index); 

38. What is Maven?
	- Maven is a dependency and build manager. Its useful because it makes adding dependencies into our project simple: we just need to know what the project information is, such as 
	repository location, project name, project organization, etc. It also makes it much easier to deploy our software, because it will handle compiling and packaging our software for 
	us. 

39. How do we include dependencies / external libraries into a Maven project?
	- We can include dependencies/external libraries into our maven projects by editing the pom.xml file in our maven projects. In this file we add the information (Maven coordinates)
	for whateve dependency we want to add. 

40. What is the purpose of the pom.xml file?
	- The purpose of the pom.xml file is to configure our maven project. It allows us to edit information directly relating to our project, such as our version number, organization ID, and 
	project name. It also allows us to add/specify dependencies associated with our project. 

41. What are the Maven project coordinates?
	- Information that allows for the unique identification of projects. Includes information such as group-id, artifact-id (project name), version, and packaging information. 

42. What is Javalin?
	- Javalin is a web framework for Java. It allows us to create web servers with Java.

43. What are the three layers in three-tiered architecture? [multitiered architecture] (https://en.wikipedia.org/wiki/Multitier_architecture)
	- Controller layer 
	- Service layer 
	- Data access layer

44. What is the purpose of the controller layer?
	- The purpose of the controller layer is to handle requests sent to the webserver. It then passes these requests on to the service layer for actual data processing. 

45. What is the purpose of the service layer?
	- The purpose of the service layer is to actual perform operations on the data received from http requests. After the controller layer passes the relevant information on to
	this layer, we then perform the desired operations. If we do not require to access our database (if we have one), then we can return directly from this layer back to the service
	layer, and then on to the client. 

46. What is the purpose of the data access layer?
	- The purpose of the data access layer is to interact with our database (if we have one). It would perform operations such as getting information, setting information, etc. 

</details> 

---

## Day 5

<details> 
<summary> Click to expand </summary> 

1. What three primary actions does a web browser perform?
	- Render HTML/CSS
	- Execute JavaScript code
	- send HTTP requests and receive HTTP responses. 

2. What is HTML?
	- Stands for [Hyper Text Markup Language] (https://en.wikipedia.org/wiki/HTML). This is a language that allows for webbrowsers to display webpages. 

3. With regards to HTML, what is an attribute?
	- An attribute is a variable associated with an element. If we think in terms of Java, it would be a data member associated with an object. The attribute is akin to the variable. 

4. What is the difference between HTML, CSS, and JavaScript?
	- HTML: Hyper Text Markup Language. CSS is Casecading Style Sheets. CSS is used for editing the styling of entire websites at a time. They allow you to edit the style of all linked
	HTML webpages at once, that way its more convenient and consistent than trying to change each individual HTML page's styling. JavaScript is a programming language used to code in dynamic 
	behavior into webpages. HTML and CSS provide no way to actually program in behavior to website, so JavaScript fills in that gap. 

5. Where would we store our frontend files if we wanted to host them from our Javalin-based application?
	- In our resources folder. 

6. What is Selenium?
	- Selenium is a webdriver/web automation interface. It allows us to automate behaviors on webpages. Typically used for automating the testing of website, it also has other uses, such as setting
	up bots to scalp graphics cards as soon as they go on sale. This is lucrative, if controversial, as many leading experts consider graphics cards to now be worth more than gold. 

7. How do we set up Selenium in order to go to Google.com?
	- Once we set up our WebDriver object from selenium's Java package, we can get set a specific URL for it to go to. In this case it would be "https://www.google.com/"

8. What Selenium locators do we have?
	- "Easy" locators 
		* name	
		* id	
		* class 
		* link text
		* partial link text
		* tag name
	- "Hard" locators 
		* XPath 
		* CSS 

9. What method in Selenium allows us to type text into an element?
	- .sendKeys(String s); function

10. What method in Selenium allows us to click an element?
	- .click()
	
</details> 