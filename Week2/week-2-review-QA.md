# Week 2 Recap

## Day 1
### [Link to Day 1 powerpoint](https://github.com/211018jwa/training/blob/main/week-2/day-1/powerpoint.pdf)

* Inheritance
    - [link to examples](https://github.com/211018jwa/training/tree/main/week-2/day-1/inheritance-demo/src/com/revature/model)
        - [Animal class](https://github.com/211018jwa/training/blob/main/week-2/day-1/inheritance-demo/src/com/revature/model/Animal.java)
        - [Dog class](https://github.com/211018jwa/training/blob/main/week-2/day-1/inheritance-demo/src/com/revature/model/Dog.java)
        - [Cat class](https://github.com/211018jwa/training/blob/main/week-2/day-1/inheritance-demo/src/com/revature/model/Cat.java)
        - [Lion class](https://github.com/211018jwa/training/blob/main/week-2/day-1/inheritance-demo/src/com/revature/model/Lion.java)
* Polymorphism
    - [makeNoise overriding example](https://github.com/211018jwa/training/blob/main/week-2/day-1/inheritance-demo/src/com/revature/model/Dog.java#L11-L24)
    - [overloading example](https://github.com/211018jwa/training/blob/main/week-2/day-1/inheritance-demo/src/com/revature/model/Dog.java#L27-L38)
* Object class
    - [Java 8 Official documentation](https://docs.oracle.com/javase/8/docs/api/java/lang/Object.html)
    - [notes](https://github.com/211018jwa/training/blob/main/week-2/day-1/inheritance-demo/src/com/revature/app/Application.java#L73-L103)
    - [hashCode()](https://github.com/211018jwa/training/blob/main/week-2/day-1/inheritance-demo/src/com/revature/model/Animal.java#L32-L35)
    - [equals()](https://github.com/211018jwa/training/blob/main/week-2/day-1/inheritance-demo/src/com/revature/model/Animal.java#L37-L48)
    - [toString()](https://github.com/211018jwa/training/blob/main/week-2/day-1/inheritance-demo/src/com/revature/model/Animal.java#L50-L53)
* Downcasting refresher
    - [link](https://github.com/211018jwa/training/blob/main/week-2/day-1/inheritance-demo/src/com/revature/app/Application.java#L36-L59)

## Day 2
* Access Modifiers
    - public
    - protected
    - default
    - private
    - [link to powerpoint notes](https://github.com/211018jwa/training/blob/main/week-2/day-2/access-modifiers-and-encapsulation.pdf)
* Encapsulation
    - [link to encapsulation demo project](https://github.com/211018jwa/training/tree/main/week-2/day-2/encapsulation-demo)
        - Passing Person data around
            - data -> Service layer -> Data access layer
        - [link to person class](https://github.com/211018jwa/training/blob/main/week-2/day-2/encapsulation-demo/src/com/revature/model/Person.java#L15-L80)
    - [link to powerpoint notes](https://github.com/211018jwa/training/blob/main/week-2/day-2/access-modifiers-and-encapsulation.pdf)
* Java Bean
    - [private properties](https://github.com/211018jwa/training/blob/main/week-2/day-2/encapsulation-demo/src/com/revature/model/Person.java#L17-L20)
    - [No-args constructor](https://github.com/211018jwa/training/blob/main/week-2/day-2/encapsulation-demo/src/com/revature/model/Person.java#L22-L25)
    - [Getters and Setters](https://github.com/211018jwa/training/blob/main/week-2/day-2/encapsulation-demo/src/com/revature/model/Person.java#L35-L80)
* Non-access Modifiers
    - [general notes](https://github.com/211018jwa/training/blob/main/week-2/day-2/non-access-modifiers/src/com/revature/app/Application.java#L5-L18)
    - final keyword
        - [variable example](https://github.com/211018jwa/training/blob/main/week-2/day-2/non-access-modifiers/src/com/revature/app/Application.java#L26-L30)
        - [class example](https://github.com/211018jwa/training/blob/main/week-2/day-2/non-access-modifiers/src/com/revature/model/NonExtendableClass.java#L3)
        - [method example](https://github.com/211018jwa/training/blob/main/week-2/day-2/non-access-modifiers/src/com/revature/model/Animal.java#L21-L23)
    - static keyword
    - abstract keyword
* Abstraction
    - [general notes](https://github.com/211018jwa/training/blob/main/week-2/day-2/abstraction/src/com/revature/model/Shape.java#L3-L11)
    - Abstract class
        - [abstract class Shape](https://github.com/211018jwa/training/blob/main/week-2/day-2/abstraction/src/com/revature/model/Shape.java#L13-L39)
        - [concrete class Rectangle](https://github.com/211018jwa/training/blob/main/week-2/day-2/abstraction/src/com/revature/model/Rectangle.java)
        - [concrete class Circle](https://github.com/211018jwa/training/blob/main/week-2/day-2/abstraction/src/com/revature/model/Circle.java)
        - [concrete class Triangle](https://github.com/211018jwa/training/blob/main/week-2/day-2/abstraction/src/com/revature/model/Triangle.java)
    - Interface
        - [default keyword](https://github.com/211018jwa/training/blob/main/week-2/day-2/abstraction/src/com/revature/dao/PersonDAO.java#L19-L34)
        - [interface PersonDAO example](https://github.com/211018jwa/training/blob/main/week-2/day-2/abstraction/src/com/revature/dao/PersonDAO.java#L7-L41)
        - [dao package](https://github.com/211018jwa/training/tree/main/week-2/day-2/abstraction/src/com/revature/dao)

## Day 3
* [Independent Research](https://github.com/211018jwa/training/blob/main/week-2/day-3/wednesday-research.md)
    - Wrapper classes
        - Byte, Short, Character, Integer, Long, Float, Double, Boolean
        - Autoboxing, Unboxing
    - Collections API
        - List interface
            - ArrayList class
            - LinkedList class
        - Map interface
            - HashMap class
        - Set interface
            - HashSet class
        - Queue interface
    - Generics
        - ex. `ArrayList<Dog> listOfDogs = new ArrayList<>();`
        - `<>` syntax

# Question Practice
* What is the purpose of inheritance?
* What is a subclass / child class?
* What is a superclass / base class?
* What does the subclass inherit from the super class?
* What is the purpose of super()?
* What is method overriding?
* How is method overriding different than method overloading?
* If Dog extends Animal, can you use an Animal reference variable to point to a Dog object?
* If a method is first defined in the Dog class (not overridden from the Animal class), can we invoke that method from an Animal reference variable? If not, what do we need to do with that Animal reference variable? (hint: starts with down)
* What is special about the Object class?
* What methods does the Object class contain?
* What is the purpose of overriding the equals() method?
* If we do not override the equals() method, how does its implementation in the Object class work?
* What is the purpose of overriding the toString() method?
* If we do not override the toString() method, what does it do by default?
* When overriding the equals() method, why do we also need to override the hashCode() method?
---
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
* What are wrapper classes?
* Why do we need wrapper classes?
* What is autoboxing/unboxing?
* What is the Collections API?
* What is the Collections API hierarchy of interfaces and classes?
* Can Collections such as a List contain primitives or only objects?
* What do we mainly use generics with?