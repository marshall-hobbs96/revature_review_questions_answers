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
2. What is a media query?
3. What is the syntax for media queries?



</details> 

---

## Design Patterns

<details>

<summary> Click to Expand </summary>


1. What is the Singleton design pattern?
2. How would you create a class that follows the Singleton design pattern?
3. What is the Factory design pattern?
4. How would you implement the factory design pattern?



</details> 

---

## Java

<details>

<summary> Click to Expand </summary>


1. What is a functional interface?
2. What are functional interfaces typically used to create?
3. What are lambdas?
4. What method do we need to implement within a class that implements the Comparable interface?
5. When this method returns 0, what does it mean?
6. When this method returns a negative number, what does it mean?
7. When this method returns a positive number, what does it mean?
8. What is the purpose of the Comparator interface?


</details> 

---

## JavaScript

<details>

<summary> Click to Expand </summary>


1. What is a closure?
2. What is the purpose of call, apply, and bind?
3. What 3 ways are there to construct an object?
4. What is prototypal inheritance?
5. When an object is created using a function constructor, what property that belongs to the function constructor does the object inherit from?
6. How do we use __proto__ to make an object inherit from another object?



</details> 

---

## Agile and Scrum 

<details>

<summary> Click to Expand </summary>


1. What is the software development lifecycle?
2. What are the 7 phases of the software development lifecycle?
3. What two competing philosophies do we have?
4. What is waterfall and its characteristics?
5. What are the pros and cons of waterfall?
6. When might we use waterfall?
7. What is Agile?
8. What are the core values of Agile?
9. What are the 12 principles of Agile?
10. What are some examples of Agile frameworks/methodologies?
11. What is Scrum?
12. What is a Sprint?
13. What are the Scrum artifacts?
14. What is a product backlog?
15. Who is in charge of managing the product backlog?
16. What is the Sprint backlog?
17. How is it decided what items/user stories are included in the Sprint backlog?
18. What is a usable product increment?
19. What are user stories?
20. What is "Acceptance Criteria"?
21. What is the "Definition of Done"?
22. What is "Story Pointing"?
23. What is a burndown chart?
24. What Scrum roles are there?
25. What is the role of a Scrum Master?
26. What is the role of the product owner?
27. How large should a Scrum team be?
28. What Scrum ceremonies are there?
29. What questions should be answered by each team member during the daily standup meeting?
30. What is the difference between the Sprint Review and Sprint Retrospective meeting?



</details> 

---
