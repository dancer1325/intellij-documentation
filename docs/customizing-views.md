[//]: # (Source: https://www.jetbrains.com/help/idea/customizing-views.html)
[//]: # (Downloaded: 2025-12-17 19:23:48)

## Customize the threads view

You can customize how threads are displayed on the Frames and Threads tabs. It might be helpful when you are often navigating in the application's threads, and are interested in their specific details, such as which group a thread belongs to.

  * Right-click anywhere in the Frames or Threads tab and select Customize Threads View.

![Customize Threads View item in the menu](https://resources.jetbrains.com/help/img/idea/2025.3/debug_customize_threads.png)



Item| Description  
---|---  
Show thread groups| If this option is selected, threads appear in a hierarchy of thread groups. Having a tree-like hierarchy is useful when your program manages a number of similar threads in groups. Also, the option separates system threads from the user-defined ones, making it easier to navigate in the list.In order for a thread to appear in a particular group, use `java.lang.ThreadGroup` in your program.  
Show stack frames for synthetic methods| Specify whether you want to see stack frames for synthetic methods (the methods introduced by the compiler, which are not present in the source code). An example of such method is a method created by an inner class so that the enclosing class could access its private members.  
Move current thread to the top| Keeps the current thread on top of the list (when Show thread groups is disabled).  
Show line number| Shows the number of the line that is currently executed. This feature requires that the application is compiled with line number information.  
Show class name| Shows the name of the class containing the method. When the code inside an anonymous inner class is executed, the name of the enclosing class is displayed instead, followed by a dollar sign and a number, for example: `MyClass$1`.Keeping this option enabled is useful when you are dealing with inherited methods and there is a need to quickly differentiate between method implementations in subclasses.  
Show package name| Shows the name of the package for classes. The code in the default package is not marked. This option is only active when Show class name is enabled. Use it when there is ambiguity that class name alone does not eliminate (like `java.util.Date` vs. `java.sql.Date`).  
Show source file name| Shows the name of the source file for classes.  
Show method arguments types| Shows the types of the arguments that a method takes. This is useful when dealing with overloaded versions of the same method.
