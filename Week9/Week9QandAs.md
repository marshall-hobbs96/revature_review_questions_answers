## Hibernate
1. What is Hibernate?
	- Hibernate is a dependency that offers object relational mapping. Essentially allows us to abstracts away traditional database access. Allows us to map actual java objects
		to database tables.
		
2. What is an ORM (Object relational mapper)?
	- A framework/dependency/tool that allows us to more easily map java objects to database tables. Handles the conversion of java objects to database tables.
	
3. What is the Java Persistence API? How is Hibernate related to this API?
	- Standard java api for accessing, persisting, and managing relations between java objects and database tables. Hibernate implements/extends this api
	
4. What class and interfaces are associated w/ Hibernate?
	- Hibernate's session interface. Implements the Java Persistence EntityManager api
	
5. What are some general JPA annotations used with Hibernate to map entities?
	- @Entity: used to signify a java class has having a relation to a database table
	- @Table: allows us to explicitly name the table that the class is being mapped to. Optional
	- @Id: specifies which field of the class specified with @entity will serve as the primary key
	- @column: allows us to explicitly state the column name that a field will be associated with. Optional
	- @OneToOne, @ManyToOne, @OneToMany, @ManyToMany: allows to to specify a relationship between @entity classes
	
6. What are entities?
	- entities are just java classes that was have specified as having a relationship with a database table. 
	
7. What are some of the mapping annotations?
	- @ManyToOne, @OneToMany, @OneToOne, @ManyToMany
	
8. What are the 3 object states? Describe each of them
	- Transient: An entity object has been instantiated, but not yet persisted with the database. In this way we can actually still use our objects without actually creating a new database entry.
	- Persistent: An entity object ahs actually been created in the database as an entry. You can now modify it and see its effects reflected in the database
	- Detached: An entity that was once persistent is no longer actively associated with its associated database entry. In this way, you can modify the object without modifying its database entry. If however, you 
	persist it again, its changes will reflect in the database again. 
	
9. What is Automatic dirty checking?
	- This is when hibernate automatically saves changes made to a persistent object to the database when a transaction is commited or flushed. 
	
10. What does flushing a session do?
	- Automatically synced us the persisted object with the database
	
11. What are the different ways to retrieve data with Hibernate?
	- HQL (Hibernate query language)
	- JPQL (Java persistence query langauge)
	- SQL, traditional SQL statements
	
12. What is HQL and JPQL?
	- HQL is the hibernate specific SQL like syntax used to retrieve data from the associated database for an entity object
	- JPQL is the JPA specific SQL like syntax
	
13. What is lazy loading v. eager loading?
	- Lazy loading refers to fetching data only when it is needed. For example, only retrieving fields of an entity object when calling the getter methods for those fields. 
	- Eager loading is loading everything locally whenever an entity object is retrieve. This way, no additional querys are made behind the scenes whenever you need to access entity object fields. 
	
14. Is @ManyToOne lazily or eagerly loaded?
	- Eager
	
15. Is @OneToMany lazily or eagerly loaded?
	- Lazy
	
16. Is @OneToOne lazily or eagerly loaded?
	- Eager
	
17. Is @ManyToMany lazily or eagerly loaded?
	- Lazy
	- Basically if hibernate would potentially need to retrieve more than one other object, it is lazy loading
	
18. What is a proxy object?
	- Very lazy loading, where the object is retrieved without any of its fields retrieved. Fields are only retrieved as you need to access them.
	

## Spring
1. What is inversion of control (IoC)?
	- Inversion of control is the concept of handing off instantiation of dependent objects to the program. So if a controller layer depends on a service layer object, we would use some kind of framework to 
	hand off its instantiation. 
	
2. What is dependency injection?
	- Dependency injection is just an implemention of inversion of control. Hard to really define them separately. Just the concept of injecting dependent objects into another object. 
	
3. What is an inversion of control container?
	- Something that handles dependency injection/IOC. Such as application context or BeanFactory
	
4. What are two examples of inversion of control containers in Spring?
	- ApplicationContext
	- BeanFactory
	
5. What are the most important differences between BeanFactory and ApplicationContext? Which one is used nowadays?
	- BeanFactory lazily injects dependencies. Needs to be configured in beans.xml. Older
	- ApplicationContext eagerly injects dependecies. Can still used ApplicationContext.xml for configuration, or use annotations on specific beans, or create a specific bean configuration class. Newer
	
6. What is a Spring Bean?
	- A spring bean is simply a class that can be dependency injected. 
	
7. What is the difference between Spring Modules and Spring Projects?
	- Spring modules are the basic modules of spring. They provide all the defintions required to use different spring methods/annotations/functions. Spring projects are simply boilerplate code that implements these modules
	
8. What are some examples of Spring Modules?
	- Spring Core
	- Spring Bean
	- Spring web
	
9. What are some examples of Spring Projects? Which very important one did we use for P2 and are using for P3?
	- Spring boot, the important one
	- Spring data
	- Spring security
	
10. What 3 ways are there to configure Spring Beans?
	- XML configuration: all of our configuration for our beans in a separate XML file
	- Annotation configuration: Just configure each bean inside the bean itself
	- Java configuration: Creating a special bean configuration class. Kinda weirdly named if you ask me. Not very self explanatory
	
11. What is Java based configuration and the syntax for it? What two annotations are important for Java based configuration?
	- Java based configuration is using a special bean config class to configure all of our beans in 
	- Just use @Bean on a method to specify it as a spring bean
	- Use @configuration on the bean config class to specify it as our bean config class
	
12. What is annotation based configuration? What are the 4 "stereotype" annotations used for annotation based configuration?
	- For keeping separate classes as beans.
	- @Controller
	- @Service
	- @Component
	- @Repository
	
13. What are the 3 types of dependency injection in Spring?
	- Field injection. Just declare a field without instantiating it. Use autowire here.
	- Setter injection. Have a setter method for a field. 
	- Constuctor injection. Have the constructor handle the wiring. 
	
14. What is the purpose of the @Autowired annotation? What 3 things can we place this annotation on top of?
	- To specify that a particular field is intended to be autowired with a spring bean. Fields, constructors, setters.

## Spring Boot
1. What is Spring Boot?
	- Spring boot is a spring project that provides us boiler plate code for writing our own spring project
	
2. What does it mean for Spring boot to be `opinionated` and to have `convention over configuration`?
	- It means that the spring organization is of the opinion that using convention is better than configuring things themselves. Therefore, they provide default/automatic configuration in spring boot projects. 
	
3. How does Spring Boot's autoconfiguration work?
	- It pretty much sets up all the configuration needed to start using beans and autowiring things. How exactly it does this I don't know. I assume it just has a boilerplate xml config file or something. 
	
4. What is one way to generate a Spring boot project?
	- Just use the spring initializer webpage. It will generate a zipped maven project you can download and import. 
	
5. What is the application.properties file in a Spring Boot application?
	- A file for giving spring information on various information it needs. For example, database url, password, username. You can use it for other things as well im sure, but we've primarily used it for that. 
	
6. What are Spring Boot profiles?
	- Different application.properties presets. For example, you could have a properties for development and deployment to make things a bit easier to manage 

## Spring Data
1. Inside of the DAO layer, what object do we use to perform database related operations using JPA? (it is annotated with @PersistenceContext)
	- Entity Manager
	
2. What is a PersistenceContext?
	- It is an object that handles the different entities and possible states that they would be in
	
3. What is the purpose of the `@Transactional` annotation?
	- To notate/set/let spring know that this method will contain an entity that needs to have transactions with its associated database entry

## Spring Web
1. What is the difference between `@Controller` and `@RestController`?
	- Controller annotates a class as specifically used for handling http requests and responses. rest controller extends on this by automatically adding @ResponseBody to each return type. 
	
2. What is the purpose of `@ResponseBody`?
	- Converts a Java object being returns to a JSON object automatically
	
3. What is the purpose of `@RequestBody`?
	- Allow spring to map a json object in a request body automatically into a java 
	
4. What is the purpose of `@PathVariable`?
	- Binds path param in http requests to a variable
	
5. What is the purpose of `@RequestParam`?
	- Binds a request variable param to a variable
	
6. What 6 annotations can we place onto methods to map them to endpoints?
	- @RequestMapping
	- @GetMapping
	- @PostMapping
	- @PutMapping
	- @DeleteMapping
	- @PatchMapping
	- I assume we could use a annotation for each kind of http request? 
	
7. What design pattern does Spring Web use for controllers?
	- Model View Controller. Still kinda iffy on this one
	
8. What is the role of the DispatcherServlet?
	- Sends requests to the MVC controller

## Spring Test
1. What is the difference between unit and integration tests?
	- Unit testing tests methods in isolation, usually by mocking its dependencies. Integration testing only mocks http requests, and therefore testing the webservice as a whole.
	
2. What is an H2 database? Why do we use an H2 database for testing?
	- An H2 database is essentially a mock database. It allows us to test our webservice in isolation from our database
	
3. Where should the properties file with the settings for the H2 database go (for testing purposes)?
	- In the testing resources folder in the properties file
	
4. What is the purpose of the `@SpringBootTest` annotation? Why do we need this annotation for integration tests?
	- annotates a class as a spring boot test. Allows us to restart the application context for each test case and provides spring configuration for testing purposes.
	
5. Why might we need to use the `@DirtiesContext` annotation while doing DAO tests and integration tests?
	- So that we might start with a new application context/new mock database for each test
	
6. What is MockMvc?	
	- This allows us to mock http requests to actually test our endpoints
	

## Spring AOP
1. What is the purpose of AOP?
	- "breaking down logic into cross cutting concerns" basically if we have methods that "cut" across multiple different other methods, we can use annotations to handle these. 
	
2. What does AOP stand for?
	- Aspect oriented programming
	
3. What is an Aspect?
	- A special class that contains different "advice" methods. these methods will be used throughout other methods
	
4. What is advice?
	- A method that will be used across other methods at joinpoints
	
5. What is a pointcut expression?
	- A annotation used with advice that tells it which joinpoints to act on
	
6. What is a join point?
	- Places in other methods where we want advice to execute. 
	
7. What type of advice are there?
	- @Before
	- @After
	- @AfterReturning
	- @AfterThrowing
	- @Around
	
8. What is the the most powerful advice?
	- @Around, because it will execute before and after method execution