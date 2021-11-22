## Day 1

<details>

<summary> Click to expand </summary>

1. What is AWS RDS?
	- Stands for Amazon Web service Relational Database Service. Allows you to host databased on the "cloud". Amazon provides the server that you can host your database on, and you can set permissions on who and how it can be accessed. 
	
2. What is AWS EC2?
	- Stands for Elastic Compute Cloud. The 2 in EC2 stans for the 2 c's, not the second iteration of "EC". A service provided by Amazon that allows us to rent a server that we may run application on. Technically, we could run 
	anything we like on here, including a database. For our purposes in the scope of this curriculum, it will be used to run webservers/webservices. 
	
3. What is AWS S3?
	- S3 stands for Simple Storage Service. Again, 3 stands for the 3 s's. Used for storing data objects, such as HTML documents. For our purposes, we will be primarily using it to store our frontend (HTML, CSS, and JS files) 
	
4. How do we create an EC2 instance?
	- In our AWS account, simple go to EC2 page, and select create new instance. We should configure a few setting, like our security group/inbound rules. Unless you know what youre doing, just go with the default/free tier options. 
	
5. What is the purpose of setting inbound rules for a security group?
	- To control who can connect to our EC2 instance. Right now, we don't really have anything important on there, so we just allow anyone to connect in order to simplify the set up process. But if we were to be running a real
	web server, we would need to properly configure access to our EC2. 
	
6. How do we connect to our EC2 instance?
	- We can SSH into it. I like to use a service called [putty](https://www.putty.org/), which allows me to save details and security settings for different SSH sessions. Easier than configuring the config files and remembering
	what names I associated with each SSH host, I think. 
	- SSH is a protocol that allows us to remotely connect to different computers/servers. [Additional reading](https://en.wikipedia.org/wiki/Secure_Shell) if youre interested. [obligatory computerphile video](https://www.youtube.com/watch?v=ORcvSkgdA58&t=94s&ab_channel=Computerphile)
	
7. What is the purpose of the .pem file?
	- I'm a little shakey on what exactly the pem file is, but I believe we need it saved on our local machine because it provides security certifications and what not when we SSH to our AWS EC2 instance. Without it, (I assume)
	AWS/EC2 wouldn't be able to vertify our identity. 
	
8. What command do we use to run a .jar file as a Java application?
	- java jar application-name.jar

</details>

---

## Day 2

<details>

<summary> Click to expand </summary>

1. What are the first 3 steps in setting up Selenium?
	- Include Selenium Java as a dependecy in our POM.xml file
	- Download the appropraite chromedriver (really you could download any web browser driver, but in our cohort we'll be using chrome so, download the chromedriver)
	- Provide the location of the chromedriver.exe file within your local system System.setProperty("Webdriver.chrome.driver", "C:/whereverthefileis/chromedriver.exe")
	- Instantiate the webdriver WebDriver driver = new ChromeDriver(); 
	- Navigate to the website you want to access driver.get("http://website.com")
		* Yea I know, 5 steps, but thats what was listed in the notes and its not wrong. Just consider the last two as bonus steps

2. What Selenium locators are there?
	- I mean theres a lot...we have...
	- Standard (easy) locators 
		* name
		* Id
		* class
		* tag name 
		* link text
		* partial link text
		* I'm sure theres more...[Heres some documentation](https://www.tutorialspoint.com/selenium/selenium_locators.htm)
	- Xpath (hard) locators
	- CSS locators
	
3. What common CSS selectors are there? How can we use Selenium's By.cssSelector locator to locate elements with these CSS selectors?
	- Id: driver.findElement(By.cssSelector("#firstname"));
	- Class: driver.findElement(By.cssSelector(".firstname"));
	- Tag: driver.findElement(By.cssSelector("div"));
	- Descendant: driver.findElement(By.cssSelector("div p"));
	- Attribute: driver.findElement(By.cssSelector("div[attribute = 'value']"));
	
4. What is XPath?
	- An alternative way to find elements in an HTML webpage or DOM. Specified the path from the top of the document all the way to the target
	element. Similar to the path of files on your computer, but for web element on a page. 
		* html/body/div[1]/p[1] <- travels from the top of the document, to the html element, body element, the first div element, to the first p element. 
		
5. What is the difference between absolute XPath and relative XPath?
	- Absoulte Xpath spells out the complete path of the element you are trying to reach, similar to the example in the previous question
	- Relative Xpath allows you to skip spelling out the entire path of an element, and instead specify the partial path of an element you want to find
		* for example: //p[1] will select the first p element in the document
		
6. What is the Chropath plugin and how does it help us determine if the CSS selector or XPath selectors we are writing are valid or not?
	- It is a browser extension that will display the Xpath or CSS selector for whatever element you select in a web page. 
	
7. What is the purpose of a wait when using Selenium?
	- In order to give the JavaScript embedded within a web page time to resolve a method. If we are testing something in a webpage that has 
	results that are delivered by JavaScript, it will take time for those result to appear. At least, much longer than it would take to retrieve
	them. Therefore, we instruct selenium to wait until those results appear. Otherwise, selenium wouldn't be able to locate the results, and 
	would throw an exception. 
	
8. What 2 types of waits are there?
	- Implicit wait
	- Explicit wait
	
9. What is the difference between an implicit and explicit wait?
	- An implicit wait is a method/selenium preference that is called once at the beginning of the selenium test. It will cause all subsequant 
	selenium methods to wait for the element it is dependent on finding to appear, if it doesn't exist. 
	- Explicit wait must be defined for every selenium method that we want to wait. Because we must define it each time we want something to wait,
	it can be easier to understand what is happening within our code (self commenting) 
	
10. Which type of wait is preferable to use? Why?
	- Explicit wait, as it is more obvious what is going on to someone who is reading our code. It is self commenting (meaning we dont have to 
	make comments to explain what is happening in our code, its just kind of obvious). 
	
11. What is the page object model, what is its benefits, and how do we use it with Selenium?
	- It is a class that is primarily used in selenium testing. It is a class that stores all the xpath/css locator locations for various elements
	within a web page. This makes it easier to access these element in later tests, as we can just reference the class we created. It also makes 
	it easier to update our testing if locations change within a webpage, since we just need to change a few lines of code within our class, instead
	of having to update locators in ALL of our test methods.

</details>

---

## Day 3

<details> 

<summary> Click to expand </summary> 

1. What is BDD?
	- Stands for Behavior Driven Development. A way of approaching development by first setting out all the intended behaviors of an application. 
	Somewhat similar to user stories in AGILE. Allows for bridging the gap between development and other, non-technical parties. 
	- TDD is a part of BDD. 
	
2. What is TDD?
	- Stands for Test Driven Development. Designing the tests for an application first, then developing in order to pass these tests. 
	
3. What does it mean for BDD to be a superset of TDD?
	- It means that TDD naturally follows BDD. If you follow Behavior Driven Development, then it naturally flows into following Test Driven Development. 
	They compliment each other significantly. TDD is a part of BDD. 
	
4. How do we approach development of a feature for an application when utilizing BDD?
	- First, we define what features of our application we should have, and how they should work, in plain english. 
	- Then we follow the traditional steps of TDD, writing tests for these features/scenarios
	- Lastly, we develope our application, focusing on developing the features set out, with the goal of passing all the tests we defined earlier. 
	
5. What are the benefits of BDD?
	- Very easy to develope tests from the given scenarios
	- Allows for easier understanding of what the application can/should do, for both technical and non-technical parties.
	
6. Cucumber is a BDD framework. What 3 types of files are important to write and execute tests with Cucumber?
	- feature files
	- glue code/testing methods
	- testRunner
	
7. What is a feature file?
	- This is a file that defines an intended feature of our application, as well as all possible scenarios related to its functionality
	
8. What is a glue code/step definition file?
	- These are methods that are derived from our feature files. Extensions like Cucumber automatically generate gluecode that we can then
	use to develope test steps to be used in E2E testing of our features. 
	
9. What is the purpose of the Test Runner class?
	- This is a simple method/class that Junit can use to actually run all the test steps we've defined. 
	
10. What plugin do we need to install to Spring Tool Suite / Eclipse for running our feature files to generate the gluecode snippets?
	- Cucumber
	
11. What english-like language does Cucumber use when we define the feature files?
	- Gherkin 
	
12. What step keywords does Gherkin utilize for Scenarios?
	- Feature: for the overall feature we intend (sorry, just read the question closer and it says "Step keywords" and not just "Keywords", but these
	first two keywords are good to know anyways so I'm leaving them here)
	- Scenario: for an individual scenario/case that we expect to encounter in the use of a feature. Can be a positive or negative case
	- Given, When, And, But, Then: keywords used to define the conditions, the different individual steps taken in a scenario, 
	and the expected result

13. Write an example of a scenario using Given ... When ... Then (And and But can also be used) for the calculator app
	- ```Scenario: Add
			Given I am at the calculator app page
			When I input 5 into the left number field
			And I input 10 into the right number field
			And I click the add button
			Then I should see a result equal to 15
			```
			
14. What types of parameterization does Cucumber support?
	- Passing parameters inline 
	- Passing parameters as a table
	- Defining a scenario outline, which will run multiple times for each row of data within a table
	
15. What is inline parameterization?
	- Passing an argument directly from within the scenario definition
	
16. What is table parameterization
	- Defining the scenario, and then creating a table of variables and values afterwards

17. What is scenario outline parameterization?
	- Using a table, make the scenario run multiple times with different data

</details> 

---

## Day 4

<details> 

<summary> Click to expand </summary> 

1. What is the difference between Cucumber, Selenium, and JUnit 5? How would you describe each of these technologies? How do we use them together?
	- Cucumber is a software tool that we can use to help us use Behavior Driven Development. It allows us to define different features in feature files, different scenarios for each of those 
	features, and allows us to automatically generate test code (known as glue code) from all those different scenarios
	- JUnit5 is a testing software tool. It allows us to create test methods to test actual methods in our code. It allows us to assert what the result of a method should be, and can then automatically
	run these tests/assertions and let us know the outcome (pass, fail, exception thrown). On its own, it is primarily used for unit testing, although paired with a tool like selenium, it can be used
	to create E2E tests as well. 
	- Selenium is a software tool for automating web page actions. Primarily used to conduct E2E tests. Usually paired with a testing tool, like JUnit5
	
2. If we have only one feature file with 4 scenarios defined in it (scenario 1 has 5 steps, scenario 2 has 4 steps, scenario 3 has 4 steps, and scenario 4 has 3 steps), and then use our TestRunner file and run as JUnit test, how many tests does JUnit consider that as?
	- If we assume the steps are the same...Then only 5 steps. If they aren't the same, then 16 steps. If its a combination, it could be anywhere inbetween. This is because
	the gluecode generated is the same if the step definition is the same. So assuming you set it up right, JUnit5 would only see it as 5 tests.
	
3. Refer to the `add.feature` file [at this LINK HERE](https://github.com/211018jwa/training/blob/main/week-5/day-4/calculator-e2e-bdd-testing/src/test/java/com/revature/features/add.feature#L3-L25). Note how each of the 4 scenarios (test) has the same step, `Given I am at the calculator page`. Is there a single "step definition" in the gluecode file or multiple step definitions for this?
    - The question above is to get you thinking about the fact that you can re-use the same step in multiple scenarios in your feature files. But, the step definition/implementation itself (a method) will be a single one in the gluecode file. 
    - [example here](https://github.com/211018jwa/training/blob/main/week-5/day-4/calculator-e2e-bdd-testing/src/test/java/com/revature/tests/ArithmeticTest.java#L17-L24)
	
	- There is a single step definition
	
</summary> 
	
---

## Day 5

<details> 

<summary> Click to expand </summary>

1. How does Agile and DevOps work together in software development?
	- One of Agile's main focus' is continously delivering small, incremental, functional code. DevOps, using Continuous Integration and Continuous Delivery tools, can aid in this by creating
	pipelines from repositories all the way to deployment.  
	
2. There are three fundamental principles underpinning Agile combined with DevOps known as CI/CD. What is continuous integration, continuous delivery, and continuous deployment?
	- Continuous Integration is merging code together frequently
	- Continuous Delivery is keeping merged code in a deployable state
	- Continuous Deployment is actually continually deploying your merged code 
	
3. What is a Git branch?
	- A different branch in a repository. Like a different version of the same repository. 
	
4. When developing a new feature, should we be working directly in the `main`/`master` branch? If no, what should we do instead?
	- No, we should be working in some kind of development branch. Either a branch specifically for the feature we're working on, or a general development branch. This ties into the concept of Continuous
	Delivery. Only deliverable code should be in the main branch. However, we still want to be able to remote store code in progress in our remote repository, without breaking this rule. So we create 
	a development branch of some kind. 
	
5. Why should code be constantly merged together?
	- So that we can ensure that it all worked and is in a continuously deliverable state. So we can adhere to the Agile principal of continuously delivering small, incremental, functional code. 
	
6. Ensuring that the `main`/`master` branch is consistently in a "deliverable" state is important. What does it mean for it to be in a deliverable state? How can setting up a Github actions workflow like we saw during demos help to provide a metric on being "deliverable"?
	- Being in a deliverable state means that we can take the code that we have in our main/master branch, and actually run it without issues. An explicit example would be being able to take our Java program
	run mvn package on it, have it compiled into a jar file while passing all tests, and then being able to run that jar file without issue (though we may still have features missing).
	
7. What is Jenkins?
	- Jenkins is a DevOps tools for CI/CD. It allows us to create pipelines from our repositories to wherever we are deploying our applicaitons. It takes our code and deploys it. 
	
8. What is a Jenkins continuous delivery pipeline?
	- It is something that allows us to input a remote repository URL, create a method for when/how to grab that code, and list several bash commands we would like to execute whenever we do grab that code.
	In this way, we are creating an automated "pipeline" directly from our repository, to deployment. 
	
9. How can we use Jenkins to deploy an application "at the touch of a button"? Is this continuous delivery or continuous deployment?
	- In the above example. Provide rep URL, define method for getting code from repo, define bash commands for when code is grabbed. This is continuous deployment, because in this case we would be 
	actually deploying our code. 
	
10. How can we then completely automate Jenkins to automatically build and deploy our application whenever the `main`/`master` branch on Github changes? Is this continuous delivery or continuous deployment?
	- github web hooks. When set up, they automatically send an http request letting Jenkins know the code is ready. Once thats done, we just do the above steps that I've now listed out twice. Continuous deployment,
	because again, we are deploying our code. 
	
11. What is the difference between a development, test, pre-prod, and prod environment in relation to testing?
	- Development: for developing code that can't and/or isn't intended to be deployed/pass tests
	- Test: for testing, duh
	- pre-prod: basically user testing. Now that we know our features work, we need to make sure our features are GOOD. Also sniff our any bugs that may have slipped through the cracks. 
	- prod: Where we actually deploy our application. This is it, its now running and accessible to the end user. 
	
12. With regards to http sessions, how does the server identify who the client is when they send requests? What does the client need to possess and send along with the http request? (hint: starts with a c)
	- HTTPSessions. A cookie. 
	
13. We can set an attribute such as `currentuser` to a particular http session along with an object such as a `User` object like in the http session demo. How can this help us out with regards to protecting endpoints and tracking who is logged in?
	- Lets us keep track of what user is currently logged in by saving their info as an object in our webserver. It helps us protect endpoints and make sure we know whos logged in by....saving whos logged in? I mean,
	the question kind of answers itself...

</details> 
