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
	- We can't call the method from an animal reference variable. The only way we can call the method is if we downcast the animal variable to a dog variable first (assuming the animal variable pointed to a dog object in the first place), 
	then we can call the method. 
	
	```
	
	Animal a1 = new Dog(); 
	a1.Bark(); //wouldn't work if Bark is only defined in Dog class
	
	((Dog) a1).bark() //This WOULD work, because we're casting the Animal reference variable to a Dog variable. But we also must have a1 pointing to a real Dog object as well. 
	// even if we cast a1 to a Dog reference variable, if a1 doesn't actually point to a Dog object, it will still fail.

	Dog d1 = (Dog) a1; //This would work as well. Even though both a1 and d1 point to the same object, only d1 can call methods only defined in Dog class, because it is a Dog reference variable.
	
	//In summary: 
		//Can't called methods that aren't associated with the variable type. Unless two criteria are met:
			//The reference variable points to an object of the type that DOES have that method
			//The reference variable is cast to that type 
	
	
	```
* What is special about the Object class? 
	- The object class is the most base class there is. Every class is either a child of the Object class, or grandchildren, or great grandchildren, etc. The object class includes some basic methods which include equals(), hashCode(), and toString(); 
	Its important to override these in child classes because otherwise they may not behave in an ideal way. 
* What methods does the Object class contain?
	- Important ones (for our curriculum so far): 
		* equals(obj o)
		* hashCode()
		* toString(); 
	- Less relevant ones	
		* clone()
		* finalize()
		* getClass()
		* notify()
		* notifyAll()
		* wait()
		* wait(long timeout) 
		* wait(long timeout, int nanos) 
		
* What is the purpose of overriding the equals() method?'
	- if we don't override this method, it only checks if the two variables point to the same object or not. We usually want this to additionally check if the two variables, if they point to different objects, if the properties of each object is equal. 
* If we do not override the equals() method, how does its implementation in the Object class work?
	- Its implementation in the Object class just checks to see if two reference variables point to the same object.  
* What is the purpose of overriding the toString() method?
	- So that we can control what the toString() method will output. For example, we can make it print out the class type as well as what datamembers it includes and their current values. 
* If we do not override the toString() method, what does it do by default?
	- It will just print out the package and class of the object, as well as the hashed memory location of the object. 
* When overriding the equals() method, why do we also need to override the hashCode() method?
	- Because if we adjust our equals() method without overriding the hashCode() method, then your class will no longer work with hash based collections, such as HashMap
---
## Day 2

* What access modifiers are there?
	- Access modifiers: Allow us to restrict access to datamembers and methods from other classes [graphic] (https://static.studytonight.com/java/images/access-modifier.jpg)
		* public: datamembers or methods with this modifier can be accessed from anywhere within our project
		* protected: datamembers or methods with this modifier can be accessed from anywhere within the same package, or from any child classes of this class. 
		* default: datamembers or methods with this modifier can be accessed from anywhere within the same package
		* private: Datamembers or methods with this modifier can only be accessed from within the same class
	- [Non-access modifers] (https://stackabuse.com/non-access-modifiers-in-java/): 
		* static: datamember or method belongs to the class itself, as opposed to objects instantiated from this class
		* final: Variable values can't be changed once assigned, methods can't be overriden, classes can't be inherited
		* abstract: If used on a method in a class, then it must be implemented in any children classes. If applied to a class itself, it means it contains abstract methods 
		* synchronized: controls thread access to method/block. Won't be going over this during course. 
		* volatile: Variable value is always read from main memory, and not thread memory. Has to do with multithreading, won't be going over in class.
		* transient: variable is skipped when serializing an object. No idea what this means. 
* What is the difference between protected and default access modifiers?
	- default allows datamembers or methods with this keyword to only be accessible from within the same package. Protected has the same restriction, but additionally it allows child classes of the class to access these datamembers
	and functions as well, even if they reside outside of the package. 
* What are the four pillars of OOP?
	- inheritance
	- encapsulation
	- polymorphism
	- abstraction
* What is [inheritance](https://en.wikipedia.org/wiki/Inheritance_(object-oriented_programming))?
	- Inheritance is the concept of being able to create derived (child) classes from base (parent) classes. The derived classes ***inherit*** all the properties of the base class. You would then add additional behaviors to the child
	class to make it distinct from the parent class. 
* What is [polymorphism](https://en.wikipedia.org/wiki/Polymorphism_(computer_science))?
	- polymorphism is the concept of the same method being able to display many distinct behaviors based upon what class/object calls it and/or what arguments are passed to it. For example, the function toString(), which is present
	in every class (because all classes are derived from the Object class), displays distinct behavior depending on which types call it. the toString() function is display polymorphic behaviors here. 
* Is method overloading compile-time or runtime polymorphism, and why?
	- Method ***overloading*** is compile-time polymorphism. This is because the compiler is able to tell what the execution path would be and can convert that into byte-code instructions. 
* Is method overriding compile-time or runtime polymorphism, and why?
	- Method ***overriding*** is run-time polymorphism. This is because the JVM needs to check what the type of object is actually being pointed to. 
* What is [encapsulation](https://en.wikipedia.org/wiki/Encapsulation_(computer_programming))?
	- Encapsulation is the idea of wrapping up all the datamembers and methods of a class into one coherent unit by restricting outside access to those datamembers and methods. This is so that developers who are using this class only use it
	in the way intended. Essentially, if a developer doesn't need to access certain datamembers or methods (i.e. they are only used internally), then they should be restricted from doing so. 
	- I think a good example is a vending machine. If you want something from a vending machine, you only have access to the coin slot and the buttons to select what snack you want. All the other internal workings of the machine are
	inaccessible to you, because you have no reason to access them when you are using the vending machine as intended. 
* What is [abstraction](https://en.wikipedia.org/wiki/Abstraction_(computer_science))?
	- The idea of representing complex ideas or concepts as types/classes.
	- For example, a real world car is a very complex piece of engineering that is capable of doing many many different actions, many of which are probably not intended by the engineers. We can abstract this real world object and 
	represent it in our code by discards all the unncessary details we aren't concerned with and focusing instead just the functions and properties that we are concerned with in the scope of our program. 
* What is a Java bean?
	- A java bean is just a class that meets certain criteria set out by the oracle foundation (Company that created and maintains Java). 
		1. All properties are private. The class must use getter and setter functions for access to all properties. For example, if an class has a datamember int value;, you couldn't do class.value because it would use a private keyword.
		You would have to create a getter function called getValue(), which would return the value. It's kinda just an extra step to meet this standard that oracle set out. It's important to follow though if you ever intend for this class
		to be used by other developers, because lots of libraries depend on this standard to function properly. 
		2. A public no-args constructor. This is fairly straight forward, and if you ask me all classes should have something like this anyways, even if you don't intend for it to be a JavaBean. 
		3. Implements [Serializable] (https://docs.oracle.com/javase/8/docs/api/java/io/Serializable.html). This interface basically ensures that a class can be serialized into streams. This is a fancy way of saying that it follows the standards
		that are necessary to be able to write this class type into external files, databases, etc. 
* What are getters and setters?
	- getter: A method that returns the value of a datamember within a class. Thats it, thats all it does. Should only be one line of code inside the method. 
	- setter: same thing, but for assigning a new value to the datamember, instead of returning it. 
* What access modifier should I generally be using to achieve encapsulation?
	- Private. This makes it so a datamember or method is only accessible from within the same class. A textbook example of encapsulation. 
* What is the purpose of the static keyword?
	- To denote a datamember or method as belonging to the class itself. This means that these datamembers and/or methods can be accessed from the class name, instead of having to instantiate an object from that class in order to access them.
	Useful for classes that are intended to just house useful functions, such as Math classes. 
* What can the final keyword be used with?
	- The final keyword can be used with Classes, Variables, and Methods. 
		* Classes: Denotes that no child classes can be made from this class
		* Variables: Denotes that this variable's instantiated value is the only value it can have. Value cannot be changed.
		* Methods: Denotes that a method cannot be overridden in child classes. 
* If I make a variable final, what does that mean?
	- It means that the variable's value cannot change. 
* If a class is final, what does that mean?
	- It means that the class cannot be extended (no child classes can be derives from this class). 
* If a method is final, what does that mean?
	- It means that the method cannot be overridden by derived (child) classes. 
* Is it possible for a class to extend multiple classes?
	- No...kinda. Not directly. You can't do something like Dog extends Animal, OtherClass {}. But if Animal extends OtherClass, you can still do Dog extends Animal. Not really extending two classes, but also kinda is. You can have grandparents, but 
	you can't have two parents. Classes have asexual reproduction (if thats an appropriate analogy for me to make) 
* Is it possible for a class to implement multiple interfaces?
	- Yes. You could hypothetically implement as many interfaces as you like. 
* In what version of Java was the `default` keyword introduced for interfaces, and what is the purpose of the default keyword?
	- Java 8. The purpose of the default keyword is to provide a default implementation of a method without having to make the method abstract. This is because before this addition, if you wanted to update an interface with new methods, 
	all classes that implemented that interface would break if they didn't update with an implementation of that new method. So default was added so that this wouldn't happen and a default behavior would occur if developers didnt update 
	their implementing classes. 
* If I declare a non-static method inside an interface, what implicit modifiers does it have?
	- public and abstract
* If I declare a variable inside an interface, what implicit modifiers does it have?
	- public, static, and final 
---
## Day 3

* What are wrapper classes?
	- Wrapper classes are classes that "wrap up" primitives. They are useful for essentially turning primitive types into reference types. This is useful because in order to modify a primitive in a method, we must pass it by reference instead of by value.
	Turning a primitive into a reference type allows us to do this. Additionally, many datastructures only accept objects and not primitives. 
* Why do we need wrapper classes?
	- In order to change primitive types to object types. See answer above for why this is useful. 
* What is autoboxing/unboxing?
	- autoboxing: Changing a primitive type into its associated wrapper class type. Done automatically for many methods. 
	- unboxing: retrieving the primitive type from its wrapper object. 
* What is the Collections API?
	- The collections API is the whole of the interfaces and classes that make up the standard datastructures within Java. 
* What is the Collections API hierarchy of interfaces and classes?
	- I don't understand how this is a different question that the one above tbh. Do you want me to list all of them? That seems like a chore. [I'm just going to link a picture] (https://facingissuesonitcom.files.wordpress.com/2019/07/java-collection-framework-hierarchy.jpg?w=1920)
* Can Collections such as a List contain primitives or only objects?
	- They can only store object. However, if those objects are just wrapper objects, then collections can (indirectly) store primitives. 
* What do we mainly use generics with?
	- Generics are used mostly with methods. Its used to create multiple different methods at once. Basically, if you want a print method for a collection, but you don't want to write a whole new method for each type of object the collection could have
	you write a generic method so that no matter what the actual type of objects the collection is storing, it will have the same behavior. 