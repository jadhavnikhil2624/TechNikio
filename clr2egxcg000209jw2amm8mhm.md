---
title: ""Wrapper Classes in Java: Elevating Primitives to Code Royalty"✨🚀🦸‍♂️"
datePublished: Sat Jan 06 2024 18:30:05 GMT+0000 (Coordinated Universal Time)
cuid: clr2egxcg000209jw2amm8mhm
slug: wrapper-classes-in-java-elevating-primitives-to-code-royalty
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1704562377019/f62674f5-6e1f-49bc-b15c-9a266a1685dc.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1704565401455/c108b9c4-6397-4f04-808d-ecab037b890f.png
tags: blogging, developers, developer, motivation, full-stack-development, wemakedevs, technikio, wrapper-class

---

## **1\. Introduction:**

> Greetings, coding aficionados! Today, we embark on a journey into the often overlooked realm of Wrapper Classes in Java. These unsung heroes may seem like Clark Kents in the coding universe, but make no mistake—they hold the key to unlocking a world of possibilities and ensuring a seamless dance between primitives and objects. Join us as we unwrap the magic and discover why Wrapper Classes are the silent architects of code transcendence.

### **#CodeMagicLaughs*🚀***🤴✨

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text"><strong>There are 8 types of wrapper classes in Java with their corresponding Primitive data types.</strong></div>
</div>

 <div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text"><strong> There are 8 Wrapper classes in Java these are Boolean, Byte, Short, Character, Integer, Long, Float, and Double.</strong></div>
</div>

## **2\. Embracing the Basics: What are Wrapper Classes?**

* A Wrapper class in Java is one whose object wraps or contains primitive data types.
    
* When we create an object to a wrapper class, it contains a field and in this field, we can store primitive data types.
    
* In other words, we can wrap a primitive value into a wrapper class object.
    

## **3\. The Magic They Bring: Why Wrapper Classes Matter**

1. They convert primitive data types into objects. Objects are needed if we wish to modify the arguments passed into a method (because primitive types are passed by value).
    
2. The classes in java.util package handles only objects and hence wrapper classes help in this case.
    
3. Data structures in the Collection framework, such as [**ArrayList**](https://www.geeksforgeeks.org/arraylist-in-java/) and [**Vector**](https://www.geeksforgeeks.org/vector-vs-arraylist-java/), store only objects (reference types) and not primitive types.
    
4. An object is needed to support synchronization in multithreading.
    

**There are several reasons that we use wrapper classes in Java those are:**

1. **Objectification of Primitives:**
    

Wrapper Classes transform primitive data types into objects, enabling them to partake in object-oriented paradigms. This opens the door to using primitives in collections, generics, and other scenarios where objects are preferred.

1. **Nullability and Default Values:**
    

Wrapper Classes provide the ability to represent null values for primitive types. This is especially valuable when dealing with scenarios where the absence of data needs to be explicitly conveyed.

1. **Facilitating Collections:**
    

Java Collections, such as `ArrayList` and `HashMap`, work with objects. Wrapper Classes facilitate the inclusion of primitives in these collections, ensuring a uniform approach to storing and retrieving data.

1. **Streamlining Generics:**
    

In Java generics, only objects can be used as type parameters. Wrapper Classes allow you to use primitives seamlessly in generic classes, enhancing the flexibility and expressiveness of your code.

1. **Enabling Frameworks and APIs:**
    

Many Java frameworks and APIs operate more efficiently with objects. Wrapper Classes make it possible to integrate primitives into these frameworks without compromising the benefits of object-oriented design.

## 4\. Advantages of Wrapper Classes

1. Collections allowed only object data.
    
2. On object data we can call multiple methods compareTo(), equals(), toString()
    
3. Cloning process only objects
    
4. Object data allowed null values.
    
5. Serialization can allow only object data.
    

Below are examples of wrapper classes in Java with their corresponding Primitive data types in Java.

## **5\. Primitive Data Types and their Corresponding**

### **Wrapper Class**

| **Primitive Data Type** | **Wrapper Class** |
| --- | --- |
| char | Character |
| byte | Byte |
| short | Short |
| int | Integer |
| long | Long |
| float | Float |
| double | Double |
| boolean | Boolean |

## **6\. Autoboxing and Unboxing**

1. ### **Autoboxing**
    

The automatic conversion of primitive types to the object of their corresponding wrapper classes is known as autoboxing. For example – conversion of int to Integer, long to Long, double to Double, etc. 

```java
import java.util.ArrayList;

class Autoboxing {
    public static void main(String[] args) {
        char ch = 'a';
        Character a = ch;

        ArrayList<Integer> arrayList = new ArrayList<Integer>();
        arrayList.add(25);

        System.out.println(arrayList.get(0));
    }
}
```

1. ### **Unboxing**
    

It is just the reverse process of autoboxing. Automatically converting an object of a wrapper class to its corresponding primitive type is known as unboxing. For example – conversion of Integer to int, Long to long, Double to double, etc. 

```java
import java.util.ArrayList;

class Unboxing {
    public static void main(String[] args) {
        Character ch = 'a';
        char a = ch;

        ArrayList<Integer> arrayList = new ArrayList<Integer>();
        arrayList.add(24);

        int num = arrayList.get(0);

        System.out.println(num);
    }
}
```

### 7\. Java Wrapper Classes Example

```java
// Java program to demonstrate Wrapping and UnWrapping
// in Classes

class Technikio {
	public static void main(String[] args)
	{
		// byte data type
		byte a = 1;

		// wrapping around Byte object
		Byte byteobj = new Byte(a);

		// int data type
		int b = 10;

		// wrapping around Integer object
		Integer intobj = new Integer(b);
		
		// float data type
		float c = 18.6f;

		// wrapping around Float object
		Float floatobj = new Float(c);
		
		// double data type
		double d = 250.5;

		// Wrapping around Double object
		Double doubleobj = new Double(d);
		
		// char data type
		char e = 'a';

		// wrapping around Character object
		Character charobj = e;

		// printing the values from objects
		System.out.println(
			"Values of Wrapper objects (printing as objects)");
		System.out.println("\n Byte object byteobj: "
						+ byteobj);
		System.out.println("\n Integer object intobj: "
						+ intobj);
		System.out.println("\n Float object floatobj: "
						+ floatobj);
		System.out.println("\n Double object doubleobj: "
						+ doubleobj);
		System.out.println("\n Character object charobj: "
						+ charobj);

		/* objects to data types (retrieving data types from
		 objects) unwrapping objects to primitive datatypes
		*/ 
		byte bv = byteobj;
		int iv = intobj;
		float fv = floatobj;
		double dv = doubleobj;
		char cv = charobj;

		// printing the values from data types
		System.out.println(
			"\n Unwrapped values (printing as data types)");
		System.out.println("\n byte value, bv: " + bv);
		System.out.println("\n int value, iv: " + iv);
		System.out.println("\n float value, fv: " + fv);
		System.out.println("\n double value, dv: " + dv);
		System.out.println("\n char value, cv: " + cv);
	}
}
```

### **Output:**

> ```java
> Values of Wrapper objects (printing as objects)
> 
> Byte object byteobj: 1
> 
> Integer object intobj: 10
> 
> Float object floatobj: 18.6
> 
> Double object doubleobj: 250.5
> 
> Character object charobj: a
> 
> Unwrapped values (printing as data types)
> 
> byte value, bv: 1
> 
> int value, iv: 10
> 
> float value, fv: 18.6
> 
> double value, dv: 250.5
> 
> char value, cv: a
> ```

### **8\. Collection Integration :**

> "**Collection Integration** with Wrapper Classes simplifies the inclusion of primitive types in Java collections. Wrapper Classes, like Integer and Double, act as object wrappers for primitives, allowing seamless storage in collections. This process involves autoboxing, where primitives are automatically converted to their corresponding Wrapper Classes when added to a collection. This consistent approach enhances code readability and flexibility, making it easier to work with a diverse range of data types within Java collections."

###   
**Conclusion: Wrapping up Wrapper Classes!**

> And there you have it, folks! Our rendezvous with Wrapper Classes has been nothing short of a coding carnival. From turning plain primitives into glamorous objects to their stellar performances in collections, these wrappers know how to steal the show.
> 
> But before you start bidding farewell to our Wrapper stars🚀 Brace yourself for the upcoming interface adventure, where code collaboration takes center stage. The excitement is about to skyrocket! ✨ #JavaJourneyContinues

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">"Interfaces in Java provide a blueprint for classes, enabling multiple inheritances, defining contracts, and promoting code flexibility through abstraction." Stay Tuned✨<strong><em>🚀</em></strong></div>
</div>

### **#CodeMagicLaughs**🦸‍♂️

# ***Happy coding! 🚀***