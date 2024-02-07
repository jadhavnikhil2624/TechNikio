---
title: "Exploring Multithreading in Java: Unleashing the Power of Concurrent Programming"
datePublished: Wed Feb 07 2024 14:12:51 GMT+0000 (Coordinated Universal Time)
cuid: clsbvddmm000309jrath84aq8
slug: exploring-multithreading-in-java-unleashing-the-power-of-concurrent-programming
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1707313373965/11886562-c7b6-470a-8e88-f5e3a176d258.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1707315120362/b786070a-ad51-49d9-9796-ec042e674403.png
tags: blogging, java, developer, multithreading, full-stack-development, wemakedevs, technikio

---

### **#CodeMagicLaughs🦸‍♂️**

### **1\. Introduction:**

> **Multithreading in**[**Java**is a](https://www.javatpoint.com/java-tutorial) process of executing multiple threads simultaneously.
> 
> A thread is a lightweight sub-process, the smallest unit of processing. Multiprocessing and multithreading, both are used to achieve multitasking.
> 
> However, we use multithreading than multiprocessing because threads use a shared memory area. They don't allocate separate memory area so saves memory, and context-switching between the threads takes less time than process.

### **2\. Understanding Threads:**

> 1. **Thread**: A Thread is a very light-weight part of process.
>     
> 2. A thread is the smallest unit of execution within a process.
>     
> 3. It represents an independent path of execution in a program.
>     
> 4. Threads allow multiple tasks to run concurrently within a program, enabling parallelism and efficient resource utilization.
>     

### **3\. How to create a Thread:**

> There are two way to create a Thread:
> 
> 1. By extending Thread class.
>     
> 2. By implementing a Runnable interface.
>     
> 
> **Example:**
> 
> ```java
> // Using Thread class
> Thread thread = new Thread() {
>     public void run() {
>         // Task to be executed by the thread
>     }
> };
> thread.start();
> 
> // Using Runnable interface
> Runnable runnable = new Runnable() {
>     public void run() {
>         // Task to be executed by the thread
>     }
> };
> Thread thread = new Thread(runnable);
> thread.start();
> ```

### **4\. What is Thread LifeCycle:**

> ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1707313924724/c338990e-6511-4a03-82ca-afca3b2fb008.webp align="center")
> 
> 1. New: Thread class object is created using a new operator by using start() method.
>     
> 2. **Ready:** This Thread is ready to run after calling the start() method.
>     
> 3. **Running:** This thread from the ready state and the trhead are running.
>     
> 4. **Waiting/Blocked:** This thread is waiting state and the thread waits for another perform task.
>     
> 5. **Dead/Terminated:** A thread is in terminated or dead state when the run() method exists.
>     

### **5\. Difference Between Process and Thread:**

| **Feature** | **Process** | **Thread** |
| --- | --- | --- |
| What is it? | An instance of a program in execution. | A subset of a process; is a lightweight unit of execution within a process. |
| Synchronization | Typically requires inter-process communication and synchronization mechanisms. | Requires synchronization for shared resources among threads within the same process. |
| Resource Consumption | Generally consumes more resources (memory, CPU time) due to separate memory space. | Consumes fewer resources compared to processes. |
| Creation Time | Longer creation time as it involves allocating separate memory space and resources. | Shorter creation time since it is created within an existing process. |
| Termination Time | Longer termination time as the OS needs to reclaim memory and resources allocated to the process. | There is a shorter termination time as threads share resources and memory within the same process. |

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">Can we start a single thread twice?</div>
</div>

> No, After starting a thread, it can never be started again. In such cases, thread will run once but for second time, it will throw exception **IllegalThreadStateException.**

### **6\. Daemon Thread:**

> 1. **Background Execution**: Daemon threads are background threads that run intermittently in the background of the application to perform tasks like garbage collection, periodic maintenance, or monitoring.
>     
> 2. **Non-Essential Threads**: They are considered non-essential threads because they do not prevent the JVM from exiting if all user threads have finished execution.
>     
> 3. **Termination with JVM**: Daemon threads automatically terminate when the JVM exits, regardless of their state of execution. This behavior distinguishes them from user threads.
>     
> 4. **SetDaemon Method**: You can set a thread as a daemon by invoking the `setDaemon(true)` method before starting the thread. This method should be called before the thread starts executing.
>     
> 5. **Supporting Role**: Daemon threads often support the main execution threads by handling background tasks that don't require explicit control or management from the main program logic. They help in keeping the application running smoothly by performing housekeeping tasks.
>     
> 6. ```java
>      Thread thread = new Thread();
>      thread.setDaemon(true); // Set as daemon thread
>     ```
>     

### **7\. Deadlock:**

> 1. Deadlock describes a situation where two or more threads are blocked forever, waiting for each other.
>     
> 2. Avoid Nested Locks: A deadlock mainly happens when we give locks to multiple threds. Avoid giving a lock to multiple threads if we already have given to one.
>     

### **8\. Thread Scheduler:**

> 1. When we create the threads, they are supervised with the help of Thread Scheduler, which is the part of JVM.
>     
> 2. Thread scheduler is only resposible for deciding which thread should be executed.
>     
> 3. Thread scheduler uses two mechanisms for scheduling the threads: Preemptive and Time Slicing.
>     
> 4. Java thread scheduler also works for deciding the following for a thread:
>     
>     It selects the priority of the thread.
>     
>     It determines the waiting time for a thread
>     
>     It checks the Nature of thread.
>     

### **Conclusion:**

> In this article, we explored the fundamentals of threads with engaging examples, unraveling the essence of concurrent programming. But hold onto your hats! Our next adventure takes us deeper into the world of Java multithreading. Get ready for a journey filled with excitement, synchronization showdowns, and the art of orchestrating threads in perfect harmony. Stay tuned for a multithreading experience like no other!👨‍💻🚀🎯

### **#CodeMagicLaughs🦸‍♂️**

### **Happy coding! 🚀✨**