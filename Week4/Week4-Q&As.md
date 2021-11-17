# Week 4 Review Questions

## Day 1

<details>

<summary> Click to expand </summary>

1. What are self-closing tags v. non-self-closing tags?

	- Self closing tags, in the context of html documents, are elements that can close by themselves. For example, ```<link/>``` would be a self closing tag, because it doesn't require you to create
	a ```</link>``` tag after it. In HTML5, even the / at the end of the self closing tag is optional, so you could have a self closing tag such as ```<link>``` be valid 
	
2. What are HTML attributes? What are some examples?

	- Attributes are things associated with an element that can have values. For example, ```<a href = "google.com">click me </a>```. The attribute in the ```<a></a>``` element is href, and 
	its value is "google.com"
	
3. What is tags make up the bare-bones structure of any HTML page?

	- ```<html></html>, <head></head>, and <body></body> ```
	
4. What are some basic HTML elements that we might use?
	
	- ```<h1></h1> through <h6></h6> for various sizes of headings ```
	
	- ```<ul></ul> and <ol></ol> for unordered and ordered lists, respectively ```
	
	- ```<img src = "imagesourcefile"> to insert images (self closing tag!), <a href = "url to webpage"> text that client see/would clikc</a> to insert links to other pages```
	
	- ```<div></div> basic block element, <span></span> basic inline element ```
	
5. What is the difference between inline and block elements? What are some examples?

	- Block elements span the entire width of the page, but you can adjust them to have specific widths and heights. An example of a block element is ```<div></div>```
	- Inline elements only take up as much space as required. You cannot adjust their width or height, and they can be inline with other elements by default. An example is ```<span></span>```
	
6. What are the 3 ways we can include CSS styling for our webpage?
	
	- Inline: adjust the styling of a specific element by including attributes directly inside the element. 
	- Internal: Define a ```<style></style>``` tag within the ```<head></head>``` tag where you define styling by tag, class, id, or style attribute
	- external: Essentially the same format as internal, however, instead of including the whole styling definitions within our html code, we define them in a separate file
	which we then link to in our html page. 
	
7. What tag and what 2 attributes for that tag are required to use external CSS?
	
	- ```<link rel = "stylesheet" href = "linktocssfile.css"> ``` (another self closing tag!)
	
8. What is the difference between class and id?
	
	- Mutliple elements can have the same class. Class is a convenient way for us to group similar elements together. This way, we can assign all elements of the same class a particular styling all at once
	- Only one element can have a certain ID at once; IDs are unique. We can then set the styling for that specific element using its id. ```#some-id { color:cyan}```
	
9. Can multiple elements have the same id?

	- No, IDs are unique. 
	
10. Can multiple elements have the same class?

	- Yes
	
11. What is the syntax for the class selector in CSS?

	- ``` .class-name {whatever styling you want} ```
	
12. What is the syntax for the id selector in CSS?

	- ```#id-name {styling stuff here} ```
	
13. What is the syntax for the tag name selector in CSS?

	- ```h1 {whatever styling}``` This will apply styling to all h1 tags, unless they have more specific styling defined elsewhere
	
14. What is the descendant selector in CSS? How does the idea of parent and child elements tie into this?

	- Allows you to specify the styling of child elements of an element with a certain ID.
	- An element can have other elements inside of it. These elements inside of the first element are children elements, and the original element is the parent element. 

15. How is CSS styling propagated? Do nested child elements inherit CSS properties from its parent?

	- CSS styling is propagated through parents to children elements. Nested children inherit CSS properties from its parent, unless more specific styling is applied.  
	
16. If we have 2 conflicting styles, what is the order of specificity in which they are resolved?

	- Whichever is defined last. So if we import a css file as our styling, but we later down in the html file define different styling for the same elements, then the later styling 
	will overwrite the earler css import. 
	
17. What 4 parts make up the CSS box model?

	- Content: What actually in the element
	- Padding: transparent area around the content
	- Border: Wraps around padding and content. Can have defined colors
	- Margin: Transparent area that wraps around the border. 
	
18. What are the `px`, `em`, and `rem` units?

	- These are different way to specify sizes for different parts of the box model
	- px: pixels
	- em: relative size based on pixel size of font-size of element
	- rem: similar to em, but relates to the font-size of the ***PARENT*** element instead
	
19. How does relative and absolute positioning in CSS work?

	- Relative positioning: allows us to move an element in relation to its 'natural' position within the page. 
	- Absolute positioning: allows us to move an element in relation to its parent elemenet. Parent element positioning should be set to relative. 
	
20. What are semantic elements and what are some examples?

	- This is an element that clearly defines its meaning to the browser. They behave just like div elements, but have different names so that its more clear what they are intended for. Analogous to 
	self commenting code for html. 
	- ```<article></article>, <aside></aside>, <footer></footer>, <header></header> ```
	
21. What is CSS grid used for? How would you describe how to use it?

	- CSS grid is used for organizing elements in an html document. Its a framework that provides us an easier way to organize our elements than trying to do it manually. 
	- We can specify the number of columns and rows, as well as their sizes and space between them, and then we can fill these grid spaces with element. 
	
22. What are the phases in the Maven build lifecycle?

	- Validate: Making sure all our dependencies are available and our pom.xml is valid
	- Compile: Compile our code into java bytecode
	- test: run any and all tests we've created
	- package: Places all our compiled code into a single .jar file
	- Integration test: runs any integration tests
	- Verify: Make sure all integration tests pass
	- install: Install our code into our local maven repository
	- Deploy: Upload our local maven repository to mvnrepository 

</details>

## Day 2

<details>

<summary> Click to expand </summary>


1. What does it mean for JavaScript to be dynamically typed?
	- It means that variables don't have a set type. You can assign var a = 1 on one line, and then later assign it a = "Hello", and the interpreter will allow this and handle it at runtime. 
	
2. Why is JavaScript called JavaScript?
	- As a marketing gimmick. At the time, Java was a very popular programming language, and the creater of JavaScript thought he could make his programming language more popular by associating it
	with Java, even though they have nothing to do with each other. 
	
3. Is JavaScript related to Java?
	- No. In name only. 
	
4. What are the 6 primary datatypes in JavaScript?
	- boolean
	- string
	- number
	- undefined
	- null
	- object 

</details>

##Day 3

<details>

<summary> Click to expand </summary>

1. What 3 types of functions are there?
	- Named functions: ```function myFunction() = {do things;}```
	- Anonymous functions: ```var myVar = function() {do things;}```
	- Arrow functions: ```let myArrowFunction = (input1, input2) => {do things;}```
	
2. What does it mean for functions to be first class citizens in JavaScript?
	- It means that functions can be...
		* Returned from a funcion
		* Assigned to a variable
		* Passed around as arguments
		
3. What variable scope does let and const add?
	- Block scope
	- Previously, there was only global and function scope. 
	
4. What is ECMAScript?
	- A standard for JavaScript. Contains specifications for what the langauge should have. Stands for European Computer Manufacturers Association. 
	
5. What version of ECMAScript was let and const added in?
	- ES6
	
6. What is function hoisting?
	- Function hoisting is a feature of JavaScript, in which all variable and function declarations and implementations are "hoisted" to the top of the JavaScript file. This allows you to declare 
	a variable or function ***After*** you have already used it. (from your perspective. In actuality, the JavaScript interpreter just takes that variable/function declarartion and brings it to
	the top of the file, before anything else actually uses it. That is what "hoisting" is). 
	
7. If I declare a `var` variable in a block inside a function, will it be block or function scoped?
	- Function scoped
	
8. If I declare a `let` or `const` variable in a block inside a function, will it be block or function scoped?
	- Block scoped
	
9. Why should we use let and const instead of var?
	- Because var variables cannot be block scoped. So for example, if you needed a temporary variable to run a for loop, you would need to use let instead of var, otherwise the var variable will
	persist after the for loop terminates. You could probably get away with this if you are careful, but it still has the ability to create a bug if a developer is careless. 
	
10. What is the difference between let and const?
	- Let essentially just lets you declare a variable that can be block scoped. Const is for creating a variable whose value will not change. Similar to the final keyword in Java. 
	
11. For a regular or anonymous function, where does the `this` keyword inside the function get its meaning from?
	- In regular and anonymous functions, "this" refers to whatever object is calling a particular function. For example, if person1.greet(), then the "this" keyword would refer to person1.
	
12. For an arrow function, where does the `this` keyword get its meaning from?
	- From whatever the scope of the arrow function is. Instead of refering to the "this" of the calling object, it will refer to the "this" of the scope in which the arrow function was defined. 
	
13. What are the 3 different ways of declaring strings in JS?
	- Sinle quotes ''
	- Double quotes ""
	- Template literals (for defining a string that you can fill with arguments) ``
		* Think back to project 0 where we fill in SQL statements from a template we define. Similar scenario here, but for strings in general, not specifically SQL statements. 
		
14. What is type coercion?
	- Type coercion refers to a feature in JavaScript where, if you are comparing two values that have different types, they will be "coerced" into the same type to be compared. 
	
15. What is the difference between `==` and `===`?
	- "==" is type coerced equals. So if 10=="10", then it will resolve to true, because "10" is coerced from a string to a number. 
	- "===" is ***NOT*** type coerced. So if 10==="10", then "10" will NOT be coerced into 10, and will instead be compared a string to a number, which will therefore return false. 
	
16. How are objects structured in JS? What do they contain? 
	- Objects are structured very similarly to how objects are structured in Java. However, you don't need a class definition to make objects out of, you can just make them on the fly. 
	- Created using JSON format (makes sense, because json stands for JavaScript Object Notation). 
	
17. How do you create an object using object literal syntax?
	- let object1 = {"property1" : "hello",
					"property2" : "World"}

</details>

##Day 4

<details>

<summary> Click to expand </summary>

1. What is the difference between a path parameter and query parameter for an HTTP request?
	- A path parameter is a required field within the URI for an endpoint. I.e, if you want to delete a client in our bank API, you need to specify which id they have. If you don't include this, you
	will get a 404 not found error.
	- A query parameter will look for optional arguments in a URI. For example, when we search a client's accounts between two fund arguments. 

2. What is the DOM?
	- Document Object Model. It is a standard for accessing documents. In particular to our case, it is the way we can instruct JavaScript to travel along our HTML elements and add, delete, or modify them. 
	
3. What is DOM manipulation?
	- DOM manipulation refers to altering, adding, or deleting elements in a DOM tree. In our case, different elements within our HTML document. 
	
4. What is the `document` object in JS?
	- Document refers to the HTML file itself. 
	
5. What is the syntax in JavaScript to create an element?
	- let div = document.createElement('div'); 
	
6. What three properties can we use to modify the content of an element?
	- textContent: returns the text content of the specified node and all its descendents. [W3 link](https://www.w3schools.com/jsref/prop_node_textcontent.asp)
	- innerText: returns the text content of the specified node and all its descendents, except style and script elements. [W3 link](https://www.w3schools.com/jsref/prop_node_innertext.asp)
	- innerHTML: returns the html content of an element. [W3 link](https://www.w3schools.com/jsref/prop_html_innerhtml.asp)
	
7. What function can we use to add an element to the DOM?
	- appendChild(whateverTheChildIsCalled)

8. Using `document.querySelector(...)`, how do you select an element with an id of `some-id`?
	- querySelector('#some-id')
		* # = id
		* . = class
		* plain = tag
		
9. What is another function that belongs to document besides querySelector that allows you to select an element by its id?
	- document.getElementById(some-id) 
	
10. Using `document.querySelectorAll(...)`, how do you select A LIST of elements with a class of `some-class`?
	- querySelectAll('#some-class')
	
11. What is another function that belongs to document besides querySelectorAll that allows you to select a list of elements by a className?
	- getElementsByClassName('className')
	
12. How do you set the attributes of an element using JS?
	- variableName.style.color = 'red'
	- variableName.href = 'url'
	
13. How do you modify the CSS styling of elements using JS, and how does the naming convention of the CSS properties differ within JS compared to styling in a .css file?
	- css style: div {color : red; text-align : center }. CSS looks similar to JSON format
	- JavaScript: variableName.color = 'red'; variableName.text-align = 'center'; JavaScript looks more like Java
	
14. How are arrays in JS different than in Java?
	- Arrays are not static. They can dynamically change in size. 
	
15. What 4 functions can we utilize to add and remove elements from a JS array?
	- appendChild()
	- insertBefore()
	- replaceChild()
	- remove()
	- removeChild()
	
16. What is an event?
	- An event is something that the user does on the webpage, such as clicking a button 
	
17. What is an event listener?
	- An event listener is a special function that will call an additional method whenever an event, such as clicking a button, happens.
	
18. What is the syntax for adding an event listener to an element?
	- variableNameOfElementWeWantToListenOn.addEventListener('theEvent', theMethodWeWantToCall);
	
19. Using the idea of adding an event listener to an element, how would you be able to print to the console the message, "button clicked" whenever you click on a button?
	- button.addEventListener('click', printButtonClicked);

</details>

##Day 5

<details>

<summary> Click to expand </summary>

1. What is a "callback" function?
	- A function that is passed as an argument to another function. It is then invoked by the outer function in order to perform some action. 
	
2. What is the purpose of the JavaScript event loop?
	- To provide the illusion of multithreaded operation. Allows for multiple things to be happening at once, without having to wait for a single operation to complete from beginning to end first. 
	Very useful for web applications where responsivness is highly valued. 
	
3. What is the callback queue?
	- A queue of callback functions that are slated to be executed. This is what allows JavaScript to maintain the illusion of multithreaded operation. 
	
4. What is the fetch API?
	- An API within JavaScript that allows JavaScript to send HTTP requests and receive HTTP responses
	
5. What does the `fetch(...)` function return? (hint: starts with a P)
	- It returns a promise
	
6. What are promises in JS?
	- Just ripping this straight off [some website](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise) because it explains it really well: A Promise is a
	proxy for a value not necessarily known when the promise is created. It allows you to associate handlers with an asynchronous action's eventual success value or failure reason. 
	
7. What 2 states can a promise that is pending transition to?
	- fulfilled: operation completed successfully
	- rejected: something went wrong

8. How does .then(...) and .catch(...) work with these two states in handling a promise?
	- .then(){} handles what happens when a promise is fulfilled, i.e. completed successfully.
	- .catch(){} handles what happens when a promise is rejected, and otherwise acts as a traditional catch block would. 
	
9. How does async-await, another way to deal with promises, work?
	- It essentially does the same thing, but allows us to structure our JS code in a more traditional try...catch block fashion. You must declare any function that uses await within it as an
	async function. 

</details>