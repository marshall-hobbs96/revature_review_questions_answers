## DAY 1

<details>

<summary> Click to Expand </summary>


1. What JavaScript engine does Chrome use for executing JS in the browser?
	- V8
	
2. How can we run JS outside of the browser?
	- By utilizing Node.js
	
3. What is Node.js? What is the primary reason we need Node.js when developing Angualar applications?
	- Node.js is a runetime enviroment for JavaScript that is outside the browser. We primarily use it when developing Angular applications
	because it provides many tool for developing and running Angular projects
	
4. What is npm?
	- Node Package Manager. Provides a way to import project and developer dependencies
	- Analogous to Maven in Java
	
5. What is the importance of the package.json file?
	- A list of dependencies related to our Angular project. Includes both project dependencies and developer dependencies
	- Analogous to the pom.xml file in Maven projects
	
6. What is the scripts property in the package.json file?
	- Contain a list of scripts you can run using npm run <script name>
	
7. What command do we use to run an individual script?
	- npm run <script name> 
	
8. What is the difference between dependencies and devDependencies?
	- Dependencies are dependencies that the project requires to run. 
	- DevDependencies are dependencies that we are required to have to develop the application
	
9. What is Angular CLI used for?
	- Used for running various node commands, such as ng, which allows us to generate new things, such as new Angular projects or components for our Angular project
	
10. What does CLI stand for?
	- Command Line Interface
	
11. How do we install Angular CLI?
	- npm install -g @angular/cli
	
12. How do we create a new Angular project using Angular CLI?
	- ng new <project name> 
	
13. What is the purpose of the node_modules folder inside an Angular project or any node project?
	- Contains all the dependencies that an Angular project requires
	
14. Should the node_modules folder be pushed to Github? Why or why not?
	- No. Because it can be rather large. Also the package.json contains a list of all dependencies required, so if anyone needs to use or develop the application, they can
	just download all the dependencies themselves based off that package.json file
	
15. If another developer wants to collaborate, they need to clone the repository with the project. What command do they need to run to ensure that all necessary dependencies are installed to their local copy of the project?
	- npm install
	
16. Describe the startup/bootstrap process for an Angular application whenever it is first ran on the computer
	- Whenever an Angular SPA is loaded, it runs code in the main.ts file, and loads up the AppModule which loads up the AppComponent into the DOM
	
17. What files make up a component? Describe the purpose of these 3 files
	- <name>.component.html
		* For containing all the html for our component
	- <name>.component.css
		* For containing all of the css for our component
	- <name>.component.ts
		* Contains all our programming logic for our component
	- <name>.component.spec.ts
		* Contains unit tests for our component.ts file
		
18. What file is the @Component decorator located inside of and what 3 important properties does it have?
	- <name>.component.ts
	- Selector, which denotes which tag you should use to display this component
	- templateUrl, which points to the .html file to use with this component
	- stylesUrls, which contains a list of all the css files to use with this component
	
19. Which of the 3 @Component properties is useful for helping us figure out what tag we need to use to display a component within another component?
	- Selector

20. What is the parent-most component in an Angular app?
	- app.component 


</details> 

---

## DAY 2

<details>

<summary> Click to Expand </summary>



1. What is the syntax for declaring a variable of a particular type in TypeScript?
	- let a: string;
	- let b: any;
	- let c: boolean;
	- let d: number;
	
2. If we declare and assign some value to the variable on the same line without specifying the type explicitly of the variable, what type will that variable be? (Type inferencing)
	- The type will be of the type of the thing we are assinging it to
	- let a = "Hello";
	- a will be of type string
	
3. If we declare a variable with the any type, what does any mean?
	- It means it will behave just as a JavaScript variable, being able to be assigned any type
	
4. What would a function in TypeScript look like in terms of the parameters?
	- (a: number, b: string)
	
5. How do you specify a return type for a TypeScript function?
	- function(): number;
	
6. What return type should you specify if you create a function that doesn't return anything?
	- function(): void;
	
7. What is the syntax declare a variable with the type being a string array?
	- ```function(): string[];```
	
	
8. What is the purpose of an interface in TypeScript?
	- Provide way to create custom types
	
9. What is the shorthand syntax for a TypeScript class where we can define properties and have the constructor be able to assign values to those properties 
   without needing to type everything out explicitly?
	- constructor(public width: number, public height: number){};

10. What access modifiers does TypeScript have?
	- public: anyone can access outside of class
	- private: Can only access from within class
	- Protected: can access from within class or within subclasses
	
11. If we need to declare a variable with a type being an object with a massive number of properties or complicated nested structures, especially if other variables 
    will be using that same type, what is the best practice in creating a "type" for it?
	-	Be as neat as you can? Provide as much documentation as you can? This is a very generic question



</details> 

---

## DAY 3

<details>

<summary> Click to Expand </summary>


1. What types of one-way databinding are there?
	- One-way databinding is the process of sending data from the .ts file to the .html file of a component, or vice versa
	- String interpolation
	- Property binding
	- Event binding
	
2. What is the purpose of string interpolation, and what is the syntax?
	- To pass information from the component class (.ts file) to the component template (html file)
	- {{nameOfVariableOrFunction}}
	
3. What is the purpose of property binding, and what is the syntax?
	- To pass information from the class (.ts) to an attribute of an element in the template (html file)
	- <div [name] = "someVariableInTsFile"></div>
	
4. What is the purpose of event binding, and what is the syntax?
	- Kinda like event handling, but we define the event in the template(html) and point it towards a function we would like to perform when that event
	occurs in the class (ts) file
	- (event) = "nameOfFunction($event)"
	
5. What lifecycle hooks are part of the component lifecycle?
	- constructor: Sets initial properties of component
	- ngOnChanges(): Called whenever an @input property is changed
	- ngOnInit(): Called when component is first initialized. As opposed to the constructor, executes when the component is actually placed on the DOM
	- ngDoCheck(): Called after ngOnChanges() and ngOnInit(). Used to implement custom actions for change detection 
	- ngOnDestroy(): Called before angular destroys a component
	
6. What is the component lifecycle?
	- Different steps a component goes though from when it is first created in the DOM to the time it is removed from the DOM
	
7. What type of HTML element is two-way databinding used with?
	- Input elements
	
8. How does two-way databinding help to simplify the process of coupling the value of input elements with a variable in the component class?
	- Eliminates the need to do both string interpolations and event binding 
	
9. What is the syntax for two-way databinding?
	- ```[(ngModel)] = "inputValue" ```
	
10. What is the process to set up two way databinding? 
	- Import FormsModule into module ts file
	- add FormsModules to the imports property of @NgModule decorator
	
11. What two types of directives are there?
	- Structural directives: used to manipulate the structor of the page itself
	- Attribute directives: used to change the attributes of elements
	
12. What are the 3 structural directives?
	- ngIf: Toggle the displaying of element in the DOM based on boolean expression
	- ngFor: Used to repear part of the html template for each item in an array
	- ngSwitch: similar to switch statements, but is used to selectively display certain elements based on certain cases being met
	
13. What is the purpose of *ngIf?
	- To toggle the displaying of elements in the DOM
	
14. What goes in the quotation marks for *ngIf=""?
	- The condition you want to test for
	
15. What is the purpose of *ngFor? What does the syntax look like?
	- Used to repear part of the html template for each item in an array
	-  ```*ngFor="let pokemon of pokemonData"```
	
16. What is the purpose of *ngSwitch and what is its syntax?
	- similar to switch statements, but is used to selectively display certain elements based on certain cases being met
	- ```  *ngSwitchCase="'pending'" ```
	
17. What are the 2 attribute directives?
	- ngClass
	- ngStyle
	
18. What is the purpose of each of the 2 attribute directives?
	- To change the class of an element
	- To change the various css properties of an element 



</details> 

---

## DAY 4

<details>

<summary> Click to Expand </summary>


1. What is a pipe?
2. What are some examples of built-in Angular pipes?
3. What is the purpose of a pipe?
4. What 2 decorators are used to facilitate component to component communication?
5. Is @Input used to pass data from a parent component to child component, or is it child component to parent component?
6. Is @Output used to pass data from a parent component to child component, or is it child component to parent component?
7. Is @Input associated with property binding or event binding?
8. Is @Output associated with property binding or event binding?
9. How do you create a service using Angular CLI?
10. What decorator does a service have?
11. What does it mean to have @Injectable on a service?
12. What does it mean for these services to be singletons?
13. What is dependency injection?
14. What do we need to do to inject a service into a component?
15. What is the name of the service that our custom created services will need to have injected into them in order to send HTTP Requests in Angular?
16. How do we get HttpClient working? What module needs to be imported into our App Module?
17. What is the purpose of routing in Angular? How does this relate to the idea of Angular being a single page application framework?
18. Where do we specify routes in the Angular application?
19. What is the reason you might use a route guard?
20. What is a subject?
21. What is an observable?
22. What is the difference between an observable and promise?
23. What does HttpClient return for HTTP requests being made?



</details> 

---