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
4. What is XPath?
5. What is the difference between absolute XPath and relative XPath?
6. What is the Chropath plugin and how does it help us determine if the CSS selector or XPath selectors we are writing are valid or not?
7. What is the purpose of a wait when using Selenium?
8. What 2 types of waits are there?
9. What is the difference between an implicit and explicit wait?
10. Which type of wait is preferable to use? Why?
11. What is the page object model, what is its benefits, and how do we use it with Selenium?

</details>

---

## Day 3

<details> 

<summary> Click to expand </summary> 

1. What is BDD?
2. What is TDD?
3. What does it mean for BDD to be a superset of TDD?
4. How do we approach development of a feature for an application when utilizing BDD?
5. What are the benefits of BDD?
6. Cucumber is a BDD framework. What 3 types of files are important to write and execute tests with Cucumber?
7. What is a feature file?
8. What is a glue code/step definition file?
9. What is the purpose of the Test Runner class?
10. What plugin do we need to install to Spring Tool Suite / Eclipse for running our feature files to generate the gluecode snippets?
11. What english-like language does Cucumber use when we define the feature files?
12. What step keywords does Gherkin utilize for Scenarios?
13. Write an example of a scenario using Given ... When ... Then (And and But can also be used) for the calculator app
14. What types of parameterization does Cucumber support?
15. What is inline parameterization?
16. What is table parameterization
17. What is scenario outline parameterization?

</details> 

---

## Day 4

<details> 

<summary> Click to expand </summary> 

1. What is the difference between Cucumber, Selenium, and JUnit 5? How would you describe each of these technologies? How do we use them together?
2. If we have only one feature file with 4 scenarios defined in it (scenario 1 has 5 steps, scenario 2 has 4 steps, scenario 3 has 4 steps, and scenario 4 has 3 steps), and then use our TestRunner file and run as JUnit test, how many tests does JUnit consider that as?
3. Refer to the `add.feature` file [at this LINK HERE](https://github.com/211018jwa/training/blob/main/week-5/day-4/calculator-e2e-bdd-testing/src/test/java/com/revature/features/add.feature#L3-L25). Note how each of the 4 scenarios (test) has the same step, `Given I am at the calculator page`. Is there a single "step definition" in the gluecode file or multiple step definitions for this?
    - The question above is to get you thinking about the fact that you can re-use the same step in multiple scenarios in your feature files. But, the step definition/implementation itself (a method) will be a single one in the gluecode file. 
    - [example here](https://github.com/211018jwa/training/blob/main/week-5/day-4/calculator-e2e-bdd-testing/src/test/java/com/revature/tests/ArithmeticTest.java#L17-L24)
	
</summary> 
	
---

## Day 5

<details> 

<summary> Click to expand </summary>

1. How does Agile and DevOps work together in software development?
2. There are three fundamental principles underpinning Agile combined with DevOps known as CI/CD. What is continuous integration, continuous delivery, and continuous deployment?
3. What is a Git branch?
4. When developing a new feature, should we be working directly in the `main`/`master` branch? If no, what should we do instead?
5. Why should code be constantly merged together?
6. Ensuring that the `main`/`master` branch is consistently in a "deliverable" state is important. What does it mean for it to be in a deliverable state? How can setting up a Github actions workflow like we saw during demos help to provide a metric on being "deliverable"?
7. What is Jenkins?
8. What is a Jenkins continuous delivery pipeline?
9. How can we use Jenkins to deploy an application "at the touch of a button"? Is this continuous delivery or continuous deployment?
10. How can we then completely automate Jenkins to automatically build and deploy our application whenever the `main`/`master` branch on Github changes? Is this continuous delivery or continuous deployment?
11. What is the difference between a development, test, pre-prod, and prod environment in relation to testing?
12. With regards to http sessions, how does the server identify who the client is when they send requests? What does the client need to possess and send along with the http request? (hint: starts with a c)
13. We can set an attribute such as `currentuser` to a particular http session along with an object such as a `User` object like in the http session demo. How can this help us out with regards to protecting endpoints and tracking who is logged in?

</details> 
