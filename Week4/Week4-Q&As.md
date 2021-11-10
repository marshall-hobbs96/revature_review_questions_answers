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

<details>