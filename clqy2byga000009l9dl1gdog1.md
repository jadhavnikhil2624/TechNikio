---
title: "Unveiling the Java Mystique: 
Discover Java's Inheritance Magic! 🚀🧙‍♂️"
datePublished: Wed Jan 03 2024 17:39:13 GMT+0000 (Coordinated Universal Time)
cuid: clqy2byga000009l9dl1gdog1
slug: unveiling-the-java-mystique-discover-javas-inheritance-magic
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1704263678411/4e4ef9c1-dc67-409b-a972-48739357aef3.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1704303539560/0ab3f78b-b016-4714-8b2a-fd074db70e99.png
tags: oop, developer, motivation, inheritance, full-stack-development, blogger-1, wemakedevs, technikio, codemagiclaughs

---

## **Introduction**

Greetings, fellow coders! Today, let's embark on a captivating journey through the enchanting realm of Java's Inheritance. Buckle up as we unravel the secrets of this mystical concept that forms the backbone of object-oriented programming.

**#CodeMagicLaughs👨‍💻🚀**

### **What is Inheritance? 🤔📜**

At its essence, Inheritance is a captivating magic that allows a new class (subclass or derived class) to inherit attributes and behaviors from an existing class (superclass or base class). It's like passing down the magical wand and spells from one generation of wizards to the next.

> Inheritance is an important pillar of OOP(Object-Oriented Programming). It is the mechanism in Java by which one class is allowed to inherit the features(fields and methods) of another class.

### **Why Do We Need Inheritance? 🤷‍♂️🌟**

1. **Code Reusability:**
    
    * Inheritance enables the reuse of code from existing classes, saving time and promoting a cleaner codebase.
        
2. **Extensibility:**
    
    * It allows for extending existing classes and adding or modifying functionalities without altering the original code.
        
3. **Organized Class Hierarchies:**
    
    * Inheritance facilitates the creation of structured class hierarchies, making the code more organized and understandable.
        

### **Important Terminologies Used in Java Inheritance 📚🔍**

1. **Superclass:**
    
    * The existing class whose attributes and methods are inherited. It's like the elderly wizard passing on their knowledge.
        
2. **Subclass:**
    
    * The new class inherits attributes and methods from the superclass. Think of it as the apprentice inheriting magical abilities.
        
3. **IS-A Relationship:**
    
    * Describes the relationship between the subclass and superclass. For example, a `Dog` IS-A `Animal` in the realm of classes.
        
4. **Method Overriding:**
    
    * The process where a subclass provides a specific implementation for a method already defined in the superclass. Each wizard can add their unique touch to a shared spell.
        
5. **super Keyword:**
    
    * Used to call methods from the superclass in the subclass. It's like invoking the ancient spells from the magical scrolls.
        
6. **final Keyword:**
    
    * When applied to a class, it prevents the class from being inherited. A class that guards its magical secrets.
        
7. **Object Class:**
    
    * The ultimate superclass for all classes in Java. Every wizard, no matter how powerful, is still part of the grand order.
        
8. **extends Keyword:**
    
    * Used to declare inheritance in Java. For instance, `class Subclass extends Superclass` signifies that the `Subclass` inherits from the `Superclass`.
        

### How to use Inheritance in Java**🛠️☕**

### **Syntax :**

```java
class derived-class extends base-class  
{  
   //methods and fields  
}
```

### Example:

```java
class Wizard {
    // Base class attributes and methods
}

class Sorcerer extends Wizard {
    // Subclass inherits attributes and methods from Wizard
}
```

**Example: The Magical Creatures Kingdom 🐉🧙‍♂️**

Consider a superclass, `MagicalCreature`, with attributes like `name` and `ability`. Now, a subclass, `Dragon`, can inherit these attributes and add specific features like `wingSpan` and `breathesFire`. The magic is in the seamless extension!

**Technical Example:** In the below example of inheritance, class Bicycle is a base class, class MountainBike is a derived class that extends the Bicycle class, and class Test is a driver class to run the program.

```java
// base class
class Bicycle {
	public int gear;
	public int speed;

	public Bicycle(int gear, int speed)
	{
		this.gear = gear;
		this.speed = speed;
	}

	public void applyBrake(int decrement)
	{
		speed -= decrement;
	}

	public void speedUp(int increment)
	{
		speed += increment;
	}

	// toString() method to print info of Bicycle
	public String toString()
	{
		return ("No of gears are " + gear + "\n"
				+ "speed of bicycle is " + speed);
	}
}

// derived class
class MountainBike extends Bicycle {

	public int seatHeight;

	public MountainBike(int gear, int speed,
						int startHeight)
	{
		super(gear, speed);
		seatHeight = startHeight;
	}

	public void setHeight(int newValue)
	{
		seatHeight = newValue;
	}

	@Override public String toString()
	{
		return (super.toString() + "\nseat height is "
				+ seatHeight);
	}
}

// Test class
public class Test {
	public static void main(String args[])
	{

		MountainBike mb = new MountainBike(3, 100, 25);
		System.out.println(mb.toString());
	}
}
```

> **Explanation:**
> 
> * The `MountainBike` inherits attributes and methods from `Bicycle`.
>     
> * It adds a new feature (`seatHeight`) without modifying the base class.
>     
> * In the `main` method, a `MountainBike` object is created and its information is printed.
>     

```java
Output: 
No of gears are 3
speed of bicycle is 100
seat height is 25
```

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">This program demonstrates how a derived class can inherit and extend the functionalities of a base class, promoting code reuse and flexibility. 🚴‍♂️✨</div>
</div>

### **Types of Inheritance and Their Diagrammatic Representation 🧩📊**

### Below are the different types of inheritance

1. Single Inheritance
    
2. Multilevel Inheritance
    
3. Multiple Inheritance
    

### **1\. Single Inheritance**

* One subclass inherits from one superclass.
    

![Single Inheritance](https://cdn.hashnode.com/res/hashnode/image/upload/v1704265981748/104bcf30-a65d-4a3b-823c-9942ccf20aba.png align="right")

### **Syntax**

```java
// Base class
class BaseClass {
    // fields and methods of the base class
}

// Derived class inheriting from BaseClass
class DerivedClass extends BaseClass {
    // fields and methods specific to DerivedClass
}
```

### **Example**

```java
// Base class
class Animal {
    String name;

    // Constructor
    public Animal(String name) {
        this.name = name;
    }

    // Method to be overridden by derived classes
    public void speak() {
        System.out.println("Animal speaks");
    }
}

// Derived class inheriting from Animal
class Dog extends Animal {
    String breed;

    // Constructor
    public Dog(String name, String breed) {
        // Calling the constructor of the base class
        super(name);
        this.breed = breed;
    }

    // Overriding the speak method
    @Override
    public void speak() {
        System.out.println("Woof!");
    }
}

// Main class
public class Main {
    public static void main(String[] args) {
        // Create an instance of the Dog class
        Dog myDog = new Dog("Buddy", "Golden Retriever");

        // Access attributes from the base class
        System.out.println(myDog.name + " is a " + myDog.breed + " dog.");

        // Call the overridden method
        myDog.speak();
    }
}
```

> In this Java example, the `Dog` class extends the `Animal` class. The `Animal` class has a constructor to initialize the `name` attribute and a `speak` method meant to be overridden by derived classes.
> 
> The `Dog` class has its own constructor to initialize the `breed` attribute, and it overrides the `speak` method to provide a specific implementation for dogs. The `super(name)` is used to call the constructor of the base class within the derived class constructor. The `@Override` annotation indicates that the `speak` method in the `Dog` class is intended to override the method in the base class.

### **2\. Multilevel Inheritance**

In Multilevel Inheritance, a derived class will inherit a base class, and as well as the derived class also acts as the base class for other classes.

* One subclass becomes the superclass for another subclass.
    

![Multilevel Inheritance](https://cdn.hashnode.com/res/hashnode/image/upload/v1704266301655/8392bf66-c16d-4556-bb4d-8a581ddfcb4c.png align="center")

### Syntax

```java
// Base class
class BaseClass {
    // fields and methods
}

// Intermediate class derived from BaseClass
class IntermediateClass extends BaseClass {
    // fields and methods
}

// Derived class inheriting from IntermediateClass
class DerivedClass extends IntermediateClass {
    // fields and methods specific to DerivedClass
}
```

### **Example**

```java
// Base class
class Animal {
    String name;

    // Constructor
    public Animal(String name) {
        this.name = name;
    }

    // Method to be overridden by derived classes
    public void speak() {
        System.out.println("Animal speaks");
    }
}

// Intermediate class derived from Animal
class Dog extends Animal {
    String breed;

    // Constructor
    public Dog(String name, String breed) {
        // Calling the constructor of the base class
        super(name);
        this.breed = breed;
    }

    // Overriding the speak method
    @Override
    public void speak() {
        System.out.println("Woof!");
    }
}

// Derived class inheriting from Dog
class Puppy extends Dog {
    // Constructor
    public Puppy(String name, String breed) {
        // Calling the constructor of the intermediate class
        super(name, breed);
    }

    // Additional method for Puppy
    public void play() {
        System.out.println("Puppy is playing");
    }
}
```

> In this example, `Dog` is the intermediate class derived from `Animal`, and `Puppy` is derived from `Dog`, creating a multilevel inheritance hierarchy

### **3\. Multiple Inheritance:**

* One subclass inherits from multiple superclasses.
    
* one class can have more than one superclass and inherit features from all parent classes.
    
* Please note that Java does **not** support [**multiple inheritances**](https://www.geeksforgeeks.org/java-and-multiple-inheritance/) with classes.
    
* we can achieve multiple inheritances only through [**Interfaces**](https://www.geeksforgeeks.org/interfaces-in-java/).
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1704266663326/ea61dcae-6756-418c-93d4-7754c5495dd4.png align="center")
    

### Syntax

```java
// Interface 1
interface Interface1 {
    // abstract methods
}

// Interface 2
interface Interface2 {
    // abstract methods
}

// Class implementing both interfaces
class MyClass implements Interface1, Interface2 {
    // Class implementation
}
```

### **Example**

```java
// Interface 1
interface Animal {
    void eat();
}

// Interface 2
interface Machine {
    void work();
}

// Class implementing both interfaces
class Robot implements Animal, Machine {
    @Override
    public void eat() {
        System.out.println("Robot is consuming electricity.");
    }

    @Override
    public void work() {
        System.out.println("Robot is performing tasks.");
    }
}

// Main class
public class Main {
    public static void main(String[] args) {
        // Create an instance of the Robot class
        Robot myRobot = new Robot();

        // Call methods from both interfaces
        myRobot.eat();
        myRobot.work();
    }
}
```

> * `Animal` and `Machine` are two interfaces with their own methods.
>     
> * `Robot` is a class that implements both `Animal` and `Machine` interfaces.
>     
> * The `Robot` class provides concrete implementations for the `eat` and `work` methods defined in the interfaces.
>     

### **4\. Hierarchical Inheritance**

* one class serves as a superclass (base class) for more than one subclass.
    
* This enchanting form of inheritance involves multiple subclasses inheriting from a single superclass. It's like a magical family tree where the powers flow through various branches.
    

![Hierarchical Inheritance](https://cdn.hashnode.com/res/hashnode/image/upload/v1704303208608/f9683091-b38d-4f50-803b-a4538812d664.png align="center")

### **Syntax**

```java
class Animal {
    // Animal class properties and methods
}

class Dog extends Animal {
    // Dog inherits from Animal and can add specific properties and methods
}

class Cat extends Animal {
    // Cat inherits from Animal and can add specific properties and methods
}
```

### **Example:**

```java
class Animal {
    void eat() {
        System.out.println("Animal is eating.");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Dog is barking.");
    }
}

class Cat extends Animal {
    void meow() {
        System.out.println("Cat is meowing.");
    }
}

public class TestHierarchy {
    public static void main(String[] args) {
        Dog myDog = new Dog();
        myDog.eat();  // Inherited from Animal
        myDog.bark(); // Specific to Dog

        Cat myCat = new Cat();
        myCat.eat();  // Inherited from Animal
        myCat.meow(); // Specific to Cat
    }
}
```

### **Explanation:**

> 1. **Animal Class:**
>     
>     * Defines the superclass `Animal` with a method `eat()`, representing a generic eating behavior for animals.
>         
> 2. **Dog Class:**
>     
>     * Extends `Animal`, indicating that `Dog` inherits properties and methods from `Animal`.
>         
>     * Adds a specific method `bark()` to represent the unique behavior of dogs barking.
>         
> 3. **Cat Class:**
>     
>     * Also extends `Animal`, inheriting the `eat()` method from the superclass.
>         
>     * Introduces a specific method `meow()` to represent the unique behavior of cats meowing.
>         
> 4. **TestHierarchy Class (Main Class):**
>     
>     * In the `main` method, it creates instances of both `Dog` and `Cat`: `myDog` and `myCat`.
>         
>     * Invokes the `eat()` method on both, showcasing that they inherit the generic eating behavior from the `Animal` superclass.
>         
>     * Invokes the specific methods `bark()` for `myDog` and `meow()` for `myCat`.
>         

### **5\. Hybrid Inheritance:**

* It is a mix of two or more of the above types of inheritance. Since Java doesn’t support multiple inheritances with classes, hybrid inheritance involving multiple inheritance is also not possible with classes.
    
* In this mystical combination, classes experience both multiple and hierarchical inheritance. It weaves a complex web of magical connections, allowing wizards to inherit powers from various sources.
    

![Hybrid Inheritance](https://cdn.hashnode.com/res/hashnode/image/upload/v1704303254953/9b1f45a2-57f9-4d7e-8d39-a2cfa1e64b1b.png align="center")

### **Syntax:**

```java
class Spell {
    // Spell class properties and methods
}

class Potion {
    // Potion class properties and methods
}

class MagicalCreature extends Spell {
    // MagicalCreature inherits from Spell and can add specific properties and methods
}

class Wizard extends MagicalCreature, Potion {
    // Wizard inherits from both MagicalCreature and Potion, combining their powers
}
```

### **Example:**

```java
class Spell {
    void castSpell() {
        System.out.println("Casting a magical spell.");
    }
}

class Potion {
    void drinkPotion() {
        System.out.println("Drinking a mystical potion.");
    }
}

class MagicalCreature extends Spell {
    void performMagic() {
        System.out.println("Magical creature performing additional magic.");
    }
}

class Wizard extends MagicalCreature, Potion {
    void useMagic() {
        System.out.println("Wizard using combined magical powers.");
    }
}

public class TestHybrid {
    public static void main(String[] args) {
        Wizard theWizard = new Wizard();
        theWizard.castSpell();    // Inherited from Spell
        theWizard.performMagic(); // Inherited from MagicalCreature
        theWizard.drinkPotion();  // Inherited from Potion
        theWizard.useMagic();     // Specific to Wizard
    }
}
```

> In these examples, `TestHierarchy` demonstrates Hierarchical Inheritance with `Dog` and `Cat` inheriting from the common superclass `Animal`. `TestHybrid` showcases Hybrid Inheritance with `Wizard` inheriting from both `MagicalCreature` and `Potion`.

### **Types of Relationships in Java 🤝🌐**

1. **Association:**
    
    * Objects are associated but not dependent on each other.
        
2. **Aggregation:**
    
    * Objects are associated, and one can exist independently of the other.
        
3. **Composition:**
    
    * Objects are associated, and one is part of the other.
        

**Advantages of Inheritance in Java 🚀🌈**

1. **Code Reusability:**
    
    * Inherited code can be reused, reducing redundancy.
        
2. **Efficient Code Updates:**
    
    * Updates in the superclass are reflected in all subclasses.
        

**Disadvantages of Inheritance in Java 🤷‍♀️🚧**

1. **Tight Coupling:**
    
    * Changes in the superclass may impact subclasses.
        
2. **Complexity:**
    
    * Overuse of inheritance can lead to complex hierarchies.
        

### **Conclusion:**

> Our journey through Java's Inheritance has unveiled the power of building on existing magic. Like passing on ancient spells, the `MountainBike` inherits and adds its unique flair. As we wrap this chapter, get ready for the next magical leap into Abstraction! 🌟🧙‍♂️💻 #Java #InheritanceMagic #NextStopAbstraction