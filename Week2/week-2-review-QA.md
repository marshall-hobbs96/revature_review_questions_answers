# Question Practice Week 2

## Day 1
* What is the purpose of inheritance?
	- Inheritance allows us to create derivative classes. This is useful because it allows us to build on top of existing classes, and therefore makes it easier to create new classes
	but also makes it easier to organize different classes and draw relationships between them. The purpose of inheritance is better organization, readability, the ability to build
	upon existing classes, etc. 
	- I don't know if asking what the purpose of inheritance is a good question. Better to ask what it does. At least in my mind. 
* What is a subclass / child class?
	- A subclass/child class is simply a class that builds upon an existing class. So instead of building a whole new class, if we have an existing class that does most of what we want to do
	but we would still like a few additional features, we can just create a child class of that existing class and then add the additional features we want. This saves time and helps keep our
	code organized and clean. 
* What is a superclass / base class?
	- A superclass/base class is essentially the parent class. It is a class that a child or several children classes are built upon. It sets the base behaviors that all derived (child) classes
	must display in addition to whatever additional behaviors we add. 
* What does the subclass inherit from the super class?
	- The subclass inherits literally everything. It inherits all variables and methods from the parent class, which is literally anything that can exist in java.
* What is the purpose of super()?
	- super() calls a constructor of the parent class in a child class. 
* What is method overriding?
	- Method overriding is creating new behavior for a method that was inherited from a parent class. This allows us to override what was previously described by the method in the parent class with
	new behaviors of our choosing. 
* How is method overriding different than method overloading?
	- yes. Method overloading is giving different behaviors to a method ***within a class*** based on how many and/or the type of parameters it has. Method overriding is redefining what a method that was inherited
	from a parent class should do. In essence, method overloading is adding new behaviors to an existing method in a class, method overriding is giving totally new behaviors to a method that was inherited. 
* If Dog extends Animal, can you use an Animal reference variable to point to a Dog object?
	 - Yes. This is called upcasting. It is safe and implicit. See [week 1 review on upcasting and downcasting] (https://github.com/marshall-hobbs96/revature_review_questions_answers/blob/main/Week1/week-1-review-QA.md) 
* If a method is first defined in the Dog class (not overridden from the Animal class), can we invoke that method from an Animal reference variable? If not, what do we need to do with that Animal reference variable? (hint: starts with down)
	- We can't if the variable has been assigned an animal object. However, if we upcast a dog object into the animal reference variable, we would be able to. 
* What is special about the Object class?
* What methods does the Object class contain?
* What is the purpose of overriding the equals() method?
* If we do not override the equals() method, how does its implementation in the Object class work?
* What is the purpose of overriding the toString() method?
* If we do not override the toString() method, what does it do by default?
* When overriding the equals() method, why do we also need to override the hashCode() method?
---
## Day 2

* What access modifiers are there?
* What is the difference between protected and default access modifiers?
* What are the four pillars of OOP?
* What is inheritance?
* What is polymorphism?
* Is method overloading compile-time or runtime polymorphism, and why?
* Is method overriding compile-time or runtime polymorphism, and why?
* What is encapsulation?
* What is abstraction?
* What is a Java bean?
* What are getters and setters?
* What access modifier should I generally be using to achieve encapsulation?
* What is the purpose of the static keyword?
* What can the final keyword be used with?
* If I make a variable final, what does that mean?
* If a class is final, what does that mean?
* If a method is final, what does that mean?
* Is it possible for a class to extend multiple classes?
* Is it possible for a class to implement multiple interfaces?
* In what version of Java was the `default` keyword introduced for interfaces, and what is the purpose of the default keyword?
* If I declare a non-static method inside an interface, what implicit modifiers does it have?
* If I declare a variable inside an interface, what implicit modifiers does it have?
---
## Day 3

* What are wrapper classes?
* Why do we need wrapper classes?
* What is autoboxing/unboxing?
* What is the Collections API?
* What is the Collections API hierarchy of interfaces and classes?
* Can Collections such as a List contain primitives or only objects?
* What do we mainly use generics with?