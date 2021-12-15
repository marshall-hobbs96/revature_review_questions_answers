## SonarCloud

<details>

<summary> Click to Expand </summary>


1. What is SonarCloud?
	- SonarCloud is a tool that allows collecting/displaying key code metrics, such as code coverage provided by tests, code smells (potential issues within the code. Not necessarily catastrophic problems, but things that 
	could be done better), and bugs. 
	
2. What is the process in setting up SonarCloud code scanning for a repository?
	- Setting up github actions that allow for linking SonarCloud to our github repo, adding SonarCloud dependency to the POM.xml of our project, linking a test metric collection dependency, such as JaCoCo, which will
	allow us to actually collect our test metrics and provide them to SonarCloud
	
3. What is Github Actions?
	- Github actions are settings that you can use to provide instructions that should be carried out whenever code is pushed to a github repository. For example, you could provide command line instructions that will
	execute mvn package on your projects whenever you push them to github
	
4. What does the build.yml file do in the context of Github Actions?
	- the build.yml file is where you actually provide instructions to execute whenever you push code to a github repository, or some other similar event. You could provide several scenarios and their corrosponding
	actions within the build.yml file
	
5. What do we set up inside the pom.xml for SonarCloud?
	- We need to add SonarCloud information to our project properties, as well as a JaCoCo plugin to our build plugins. SonarCloud provides the specific lines that need to be added whenever you attempt to set up a 
	new project on SonarCloud. JaCoCo is a simple plugin you can look up on maven repository
	
6. What is the purpose of the JaCoCo Maven plugin?
	- This plugin collects data related to our code coverage whenever we build a maven project. When used alongside SonarCloud, it provides these metrics to SonarCloud for displaying. 


</details> 

---

## Testing Concepts

<details>

<summary> Click to Expand </summary>



1. Summarizing the different testing mindset "bullet points", what is the mindset that a tester should have?	
	- Test early, test often, concentrate on the areas most likely to produce bugs, get the most coverage you can out of the smallest number of tests. You will never be bug free, nor should you try to be. There will
	always be obscure edge case bugs. Use your best judgement to weigh the benefits of chasing after these bugs vs concentrating on other, more important things
	
2. What are the phases in the testing lifecycle?
	- Requirments analysis phase
		* review project documentation, analyze requirments
	- Test planning phase
		* What to test
		* How to test 
		* When to test
		* Test plan document produced
	- Test design phase
		* Actually writing the tests
	- Test execution phase
		* Actually executing test
		* Recording results 
	- Defect reporting phase
		* Creating a defect report
		* Getting with developers to discuss results of testing
	- Test cycle closure phase
		* Reviewing test results
		* Determine if more tests need to be conducted
		
3. What is the difference between verification and validation?
	- Validation
		* Ensures we are building what we actually want. Does software meet customer needs? 
	- Verification
		* Ensures we are building software correctly and according to the design documentation
		
4. What are some of the activities involved with verification/static testing?
	- Review: Check for correctness and compeletion of documents
	- Walkthrough: Informal review of code/design documents
	- Inspection: Formal, often team wide review of code
	
5. What two sub-categories of testing is functional testing composed of?
	- Whitebox testing
	- Blackbox testing
	
6. What are the 4 specific types of tests that make up the testing pyramid?
	- Unit tests
	- Integration tests
	- End to End tests
	- User acceptance tests
	
7. What is whitebox testing?
	- This is testing that is done with knowledge of the underlying code
	- Unit testing and integration testing fall under whitebox testing, because it requires us to have knowledge of how the code actually works
	
8. What is blackbox testing?
	- This is testing that can be done without knowledge of how the code works
	- End to End testing and user acceptance testing fall under blackbox testing. These can be performed without any knowledge of how the underlying code works
	
9. Categorize unit, integration, E2E, and UAT by whether they are whitebox or blackbox for EACH
	- Whitebox
		* Unit
		* Integration
	- Blackbox
		* E2E
		* UAT
		
10. What is a positive test?
	- A test that tests whether or not a function/method performs as expected when used as intended. I.e., properly logs a user in when valid credentials are provided
	
11. What is an example of a positive test?
	- A method that is suppose to return the sum of two integers does so when provided with two integers to add
	
12. What is a negative test?
	- A test that tests whether or not a function/method gracefully failed (provides some kind of message or what not) whenever a function/method is used in a method that is not intended or desired. Such as providing
	invalid credentials when trying to log in
	
13. What is an example of a negative test?
	- Testing to make sure the method Integer.parseInt(s) throws a numberFormatException if there is no integer to parse in the string
	
14. What is exploratory testing?
	- Executing tests to discover how an existing piece of software works/behaves
	
15. What is exhaustive testing? Is it feasible? How should a tester approach testing instead?
	- Exhaustive testing is testing every conceivable input scenario. Not feasible for anything more complicated than the simpliest of programs. Testers should use equivalence partitioning or boundry testing instead.
	
16. Describe the test design strategies of equivalence partitioning and boundary testing
	- Equivalence partitioning 
		* Dividing testing parameters in general broad catergories that can cover several similar scenarios at once. I.e., instead of testing a function with every single number in existence, we can test 
		with just positive and negative numbers and zero 
	- Boundry testing
		* Test the function at the extremes. I.e., use very large numbers, numbers with many decimal places, very long strings, etc
		
17. What does re-testing mean?
	- Running tests that have previously failed in order to see if the problem has been fixed
	
18. What is regression testing? Why is regression testing important?
	- Running old test suites (that we've already passed) in order to test if new code has broken old functionality
	
19. What is smoke testing? Why should smoke testing be performed before doing regression testing?
	- Testing the most critical components. We should test these because failures on one of these tests means major that many other functions will likely not even be accessible, even if they themselves are not broken
	
20. How does regression testing relate with the objectives of DevOps?
	- DevOps has the goal of always having deliverable code. We must perform regression testing to ensure newly written code doesn't break existing code. If we don't catch issues like this, we are literally going backwards
	in development, which is the antithesis of DevOps
	
21. What is sanity testing?
	- Quick and dirty (usually manual) testing of recently written code to make sure its doing what you want. Basically just a checkup to make sure we're making progress and we're not going crazy.
	If you are consistently failing sanity checks, maybe its time to take a break and reset
	
22. What is manual testing? Do you typically need a formal structure when doing manual testing or do you just randomly play around with the application?
	- Manual testing is having someone actually perform all steps in a test procedure. Manual testing can (and often does) have formal structure in them. They can also be quite informal (see sanity check). 
	The point is we have a real actual person performing these tests, instead of writing automated tests to perform them. 
	
23. What is test automation?
	- Test automation is writing tests that can execute on their own at a click of a button. They perform the tests and record/display the results
	
24. What is non-functional testing? What two subcategories did we cover?
	- Tests that arent directly related to the outcome of software. Functional testing is asking if we can accomplish a goal, non-functional testing asks how well we did in accomplishing a goal
	- Performance testing
	- Useability testing
	
25. What is performance testing and what subcategories does it have?
	- Performance testing is testing how well our code does under different scenarios.
	- Load testing
		* How well we do with varying numbers of concurrent users
	- Stress testing
		* How well does our program perform under extreme conditions
	- Spike testing
		* How well does our program perform when there is a sudden, drastic increase in users
	- Ramp up/Ramp down testing
		* Gradually increasing then decreasing load
		
26. What is the purpose of usability testing?
	- How easy is it to actually use the application? 
	
27. What is a defect/bug?
	- A mistake that is embedded in the code
	
28. What should a tester do when they find a defect?
	- Report it. Provide as much detail about where it is, the nature of the defect, steps to solve or mitigate the defect, etc.
	
29. What are some of the fields that should be contained on a defect report?
	- ID
	- Description
	- App version
	- Steps to replicate
	- Date discovered
	- status
	- severity
	- Priority
	
30. What levels of severity can defects have?
	- Blocker
		* Further tests cannot be performed because the failure of this feature literally blocks access to other features
	- Critical
		* Main functionality is broken
	- Major
		* Major parts are broken, but most important features still work
	- Minor
		* Won't cause major issues. Spelling mistakes, things of that nature
		
31. What levels of priority can defects have?
	- High
		* Solve immediately
	- Medium
		* Solve during next dev cycle, sprint, etc.
	- Low
		* Yea we'll get to it when we get to it
		
32. How is severity and priority different?
	- Severity describes how much it effects our application or a certain feature. Priority describes how important it is we get it done now/in the future
	- For example, a critical defect of a feature that we dont even intend to deliver for several sprints may have a low priority
	
33. What are the phases of the defect lifecycle?
	- Bug discovery
	- Bug report review
	- Bug ticket assigned
	- Bug fixing begins
	- Bug fixing ends
	- Tests performed again
	- Regression testing




</details> 

---

## Responsive Web Design

<details>

<summary> Click to Expand </summary>


1. What is responsive design? How does it help us accommodate different types of devices users may be using?
	- Responsive design is the concept that frontend applications should be flexible to different user's devices. So if a user switches from desktop to a mobile device
	they should have a very similar experience. It shouldn't break the functionality or result in a messed up UI
	
2. What is a media query?
	- A media query is a special css annotation that allows for setting different css properties to the same html elements depending on what kind of device the user has. 
	
3. What is the syntax for media queries?
	- ```
		@media(max-width: 700px) {
		
			traditional css stuff
			
		}
		```
	


</details> 

---

## Design Patterns

<details>

<summary> Click to Expand </summary>


1. What is the Singleton design pattern?
	- The singleton design pattern is a design pattern for classes that stipulates that classes should only have a single instance of that class at a time. 
	- Useful for things like connections, logging, things that really shouldn't have multiple of at once
	
2. How would you create a class that follows the Singleton design pattern?
	- Have a property of a type that is itself, and have a method that returns that instance. If that instance hasnt been instantiated yet, then create it
	
3. What is the Factory design pattern?
	- The factory design pattern is a design pattern that passes the responsibility of creating new objects to a method
	- Typically used for managing several different implementations of an interface 
	
4. How would you implement the factory design pattern?
	- Create a class with a method that returns different objects of different implementations of an interface based on what arguments you pass into the method 



</details> 

---

## Java

<details>

<summary> Click to Expand </summary>


1. What is a functional interface?
	- A functional interface is an interface that includes only one abstract method
	
2. What are functional interfaces typically used to create?
	- Typically used for implementing lambda functions
	
3. What are lambdas?
	- Lambdas are functions that are defined and return in the same place. Very similar to arrow functions in javascript. You define it, and it returns the result immediately where you defined it.
	
4. What method do we need to implement within a class that implements the Comparable interface?
	- compareTo
	
5. When this method returns 0, what does it mean?
	- It means that the two objects being compared are the same
	
6. When this method returns a negative number, what does it mean?
	- It means that the current object (this one => object1.compareTo(object2)) is "less than" the object its comparing to. This means it should go before object2 in an ordered list
	
7. When this method returns a positive number, what does it mean?
	- The opposite as above. It means that object1 is more than object2, which means it should go after object2 in an ordered list
	
8. What is the purpose of the Comparator interface?
	- To defined alternative ways to order objects of a certain type. For example, the comparable interface defines the natural ordering of objects of a class, but if we want to order
	them in different ways, we can implement the comparable interface. 


</details> 

---

## JavaScript

<details>

<summary> Click to Expand </summary>


1. What is a closure?
	- A closure it the combination of a function with its lexical enviroment. It essentially allows the persisting of varibales within a function from outside the function. 
	
2. What is the purpose of call, apply, and bind?
	- Call allows us to borrow a method from another object without specify a new property in our object
	- Apply is same as call, but uses a single array of parameteres instead of varargs
	- Bind allows you to permanently associate a call line to a new variable
	
3. What 3 ways are there to construct an object?
	- Object literals
	- Function constructors
	- ES6 classes
	
4. What is prototypal inheritance?
	- Allows you to add additional properties to function constructors that objects instantiated from it will inherit
	
5. When an object is created using a function constructor, what property that belongs to the function constructor does the object inherit from?
	- prototype 
	
6. How do we use __proto__ to make an object inherit from another object?
	- object.__proto__ = Class.prototype
	- Even if object is not related to Class, object will inherit Class' prototype behaviors



</details> 

---

## Agile and Scrum 

<details>

<summary> Click to Expand </summary>


1. What is the software development lifecycle?
	- A series of steps/states that an application goes through during its lifetime
	
2. What are the 7 phases of the software development lifecycle?
	- Planning
	- Analysis
	- Design
	- Development
	- Testing
	- Implementation
	- Maintainence
	
3. What two competing philosophies do we have?
	- Agile 
	- Waterfall
	
4. What is waterfall and its characteristics?
	- Waterfall is going through each step in the SDLC before going to the next step, and never going back to a previous step
	- Essentially, do everything "perfectly" to completition on each step, then move on to the next step

5. What are the pros and cons of waterfall?
	- Pros are that its easier to organize when dealing with large organizations/projects and when the project requirements likely won't change
	- Cons are its not very flexible and bad for dynamic projects. Also not very good for projects that require small, iterative deliverables
	
6. When might we use waterfall?
	- If we were working on a large project with very clear, restricted, inelastic requirments, such as government projects or projects in highly regulated industries
	
7. What is Agile?
	- Agile is a philosophy for going through the SDLC that essentially says we should go through the SDLC for small parts of a project over and over again. This way we can complete
	small features of a project and deliver it piece by piece, eventually working up to delivering the full application
	
8. What are the core values of Agile?
	- Individuals and interactions over processes and tools
	- Working software over comprehensive documentation
	- Customer collaboration over contract negotation
	- Responding to change over following a plan
	
9. What are the 12 principles of Agile? (Im just going to straight up copy paste this. I doubt anyone is going to ask us to remember any of these off the top of our head) 
	- Our highest priority is to satisfy the customer through early and continuous delivery of valuable software.
	- Welcome changing requirements, even late in development. Agile processes harness change for the customer’s competitive advantage.
	- Deliver working software frequently, from a couple of weeks to a couple of months, with a preference to the shorter timescale.
	- Business people and developers must work together daily throughout the project.
	- Build projects around motivated individuals. Give them the environment and support they need, and trust them to get the job done.
	- The most efficient and effective method of conveying information to and within a development team is face-to-face conversation.
	- Working software is the primary measure of progress.
	- Agile processes promote sustainable development. The sponsors, developers, and users should be able to maintain a constant pace indefinitely.
	- Continuous attention to technical excellence and good design enhances agility.
	- Simplicity–the art of maximizing the amount of work not done–is essential. 
	- The best architectures, requirements, and designs emerge from self-organizing teams.
	- At regular intervals, the team reflects on how to become more effective, then tunes and adjusts its behavior accordingly.

10. What are some examples of Agile frameworks/methodologies?
	- Scrum
	- Kanban

11. What is Scrum?
	- Scrum is an agile framework/methodology
	
12. What is a Sprint?
	- A sprint is essentially a self contained iteration of the SDLC for a set of features that are a part of the the overall application
	- Usually takes anywhere between 1 to 2 weeks
	
13. What are the Scrum artifacts?
	- Documentation relating to a sprint
	
14. What is a product backlog?
	- The product backlog is a comprehensive list of features/tasks related to the overall application. Essentially a giant to-do list for the project
	
15. Who is in charge of managing the product backlog?
	- The product owner (not actually the end-client of the application you are developing, but likely a product manager. Just someone in charge of the overall project)
	
16. What is the Sprint backlog?
	- A list of features/tasks that need to be completed for the current sprint. Items not completed on this during the current sprint will roll over into the next sprint
	
17. How is it decided what items/user stories are included in the Sprint backlog?
	- Decided upon by the team of developers
	
18. What is a usable product increment?
	- The actual product developed at the end of a sprint. It must potentially be deliverable to the end user
	
19. What are user stories?
	- User stories are features to be developed, written from the perspective of the end user
	
20. What is "Acceptance Criteria"?
	- Acceptance criteria is criteria that defines what it means for a userstory/feature to be acceptable
	
21. What is the "Definition of Done"?
	- Defined by the scrum team. It defines when a features is considered done
	
22. What is "Story Pointing"?
	- A way of assigning a difficulty to a task. Helps in managing time. Essentially a made up point system that the scrum team agrees on 
	
23. What is a burndown chart?
	- A burndown chart is a chart that tracks how many tasks/story points are remaining on the y axis and how much time has passed on the x axis
	- Just a team tool for tracking progress
	
24. What Scrum roles are there?
	- Scrum master
	- product owner
	- team member
	
25. What is the role of a Scrum Master?
	- To be responsible to ensuring that the scrum development process is being followed
	- Leading any team meetings
	
26. What is the role of the product owner?
	- To determine what should be on the product backlog 
	
27. How large should a Scrum team be?
	- 10 or fewer people 
	
28. What Scrum ceremonies are there?
	- Sprint planning meeting
	- Daily standup meeting
	- Sprint review meeting
	- Sprint retrospective
	
29. What questions should be answered by each team member during the daily standup meeting?
	- What they got done yesterday
	- What they plan on getting done today
	- Any blockers? 
	
30. What is the difference between the Sprint Review and Sprint Retrospective meeting?
	- Sprint review is for discussing what was accomplished in the last sprint and what the team hopes to accomplish for the next sprint
	- Sprint retrospective is for discussing what improvements could be made as a team based on the performance of the last sprint


</details> 

---
