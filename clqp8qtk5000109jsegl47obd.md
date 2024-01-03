---
title: "Introduction to Object-Oriented Programming (OOPs) in Java"
datePublished: Thu Dec 28 2023 13:28:49 GMT+0000 (Coordinated Universal Time)
cuid: clqp8qtk5000109jsegl47obd
slug: introduction-to-object-oriented-programming-oops-in-java
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1703768376112/240fce80-d3ac-4849-a781-72f000d0daf0.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1703770110387/93b27db7-410d-431f-96c7-146d6696ba1e.png
tags: oop, developer, motivation, full-stack-development, technical-writing-1, technikio

---

## **Introduction:**

1. Object-Oriented Programming (OOP) is not just a programming paradigm; it's a methodology that empowers developers to create robust, modular, and maintainable code.
    
2. In this article, we'll embark on a journey through key OOP concepts in Java, starting with classes, objects, the `new` keyword, and the ever-present `this` keyword.
    

As we unfold the basics, we'll glimpse into the four pillars of OOP, offering a sneak peek into what lies ahead empowering you to create scalable and modular solutions. Let's dive into the world of Java OOP! 🚀📚

## **What is OOP?**

> ***OOP is a programming paradigm that believes in grouping data (properties) and methods (actions) together inside a box. It demonstrates the pattern of real-world objects.***

**1.** [**Class-based languages**](https://en.m.wikipedia.org/wiki/Class-based_programming).  
**2.** [**Prototype-based languages**](https://www.techopedia.com/definition/30040/prototype-based-programming).

So if you are coming from C++ or Javascript, you are familiar with Class-Based syntaxes.

Java is a [**Class-based**](https://en.m.wikipedia.org/wiki/Class-based_programming) Programming Language!

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">Class-based is the mechanism by which Java creates objects on class blueprints.</div>
</div>

## **Classes and Objects:**

Classes and objects form the backbone of OOP.

What is `class` a keyword in Java?

"The `class` keyword in Java simplifies class-based inheritance, offering a cleaner syntax for creating and organizing objects. It is a syntactic improvement over the traditional Java class structure."

* `Class`**:** A blueprint or template encapsulating attributes and methods.
    

```java
public class Car {
    String make;
    String model;

    public void startEngine() {
        System.out.println("Engine started for " + make + " " + model);
    }//End startEngine
}//End class
```

`Object`**:** An instance of a class representing a real-world entity.

```java
public class Main {
    public static void main(String[] args) {
        // Creating a car object
        Car myCar = new Car();
    }//End main
```

## The basic example for a class in Java is as follows:

**Here's a simple Java program that uses a class. In this example, we'll create a class called** `Car` **with attributes and a method:**

```java
public class Car {
    // Attributes
    String make;
    String model;
    int year;

    // Constructor to initialize the car's attributes
    public Car(String make, String model, int year) {
        this.make = make;
        this.model = model;
        this.year = year;
    }

    // Method to display information about the car
    public void displayInfo() {
        System.out.println("Car Make: " + make);
        System.out.println("Car Model: " + model);
        System.out.println("Year: " + year);
    }

    public static void main(String[] args) {
        // Creating an instance of the Car class
        Car myCar = new Car("Toyota", "Camry", 2022);

        // Calling the displayInfo method to show information about the car
        myCar.displayInfo();
    }
}

```

## **Explanation:**

* We have a class `Car` with attributes (`make`, `model`, `year`) representing information about a car.
    
* The constructor (`public Car`) initializes the attributes when a new `Car` the object is created.
    
* The `displayInfo` method prints information about the car to the console.
    
* In the `main` method, we create an instance of the `Car` class named `myCar` with specific attributes and call the `displayInfo` method to show information about the car.
    

This simple program demonstrates the concept of a class in Java, encapsulating data and behavior related to a car.

### Now, Let's do the same thing with `new` keyword and see what happens:

```java
// Class definition
class Car {
    String model;

    // Constructor
    public Car(String modelName) {
        model = modelName;
    }
}

// Creating an instance using the new keyword
Car myCar = new Car("Toyota");
```

> In Java, the `new` keyword is used to create an instance of a class. It allocates memory for the object, initializes its attributes (if any), and returns a reference to the newly created object. Essentially, `new` is used to instantiate objects from a class blueprint.

# Why the '`new`' keyword in Java?

1. The `new` keyword in Java is like a creator button.
    
2. When you want a new thing (object) based on a design (class), you press `new`.
    
3. It ensures the thing is ready to use, and you get a special tag (reference). It's how you make stuff happen in Java.
    

### **Internal Working of** `new` **:**

When you use the `new` keyword with a constructor function, the following steps take place:

1. A new empty object is created. This new object will become the instance of the constructor function.
    
2. The `this` keyword inside the constructor function is set to point to the newly created object. This allows the constructor function to refer to and set properties on the newly created instance.
    
3. The constructor function executes, and any properties or methods defined with `this` inside the constructor is added to the new instance.
    
4. If the constructor function does not explicitly return an object, the new instance created `new` is returned as the result of the `new` expression. This allows you to store the created instance in a variable and use it later.
    

## `this` keyword in Java

`this` brings clarity by distinguishing between variables.

Refers to the current instance of the class.

```java
public class Car {
    String make;

    public void setMake(String make) {
        // Using "this" to refer to the instance variable
        this.make = make;
    }//End setMake
```

**Next, the Four Pillars of OOP:** Before we conclude, let's introduce the four pillars of OOP:

* **Encapsulation:** Bundles data and methods into a single unit.
    
* **Inheritance:** Establishes relationships between classes.
    
* **Polymorphism:** Enables objects to take multiple forms.
    
* **Abstraction:** Simplifies complex systems.
    

Stay tuned for our next article, where we'll unravel the depth of each pillar.

## **Conclusion:**

### As we navigate this wild world of Java OOP, we've laid the groundwork for understanding classes, objects, `new` and `this`. Get ready for the superhero showdown in the next articles, where we'll unveil the true powers of OOP in Java. 🦸‍♂️💻✨

---

> Hold onto your coding capes, heroes! The OOP journey is just getting started! 🚀

# Happy coding! 🚀