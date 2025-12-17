[//]: # (Source: https://www.jetbrains.com/help/idea/structural-search-and-replace-examples.html)
[//]: # (Downloaded: 2025-12-17 20:03:27)

## Example pattern

Let's start with a simple task and search for an open lock objects using the `synchronized` keyword. The `synchronized` keyword can have two cases:

  * as a block statement 

class ClassA { public void someMethod() { synchronized(this) { // ... } } } 

  * as a method modifier 

class ClassA { public synchronized void someMethod() { // ... } } 




Let's look for something like that

synchronized ($parameter$){ $statement$; } 

We can add the Count modifier for the $parameter$ variable form 0 to infinity. So, the pattern can search for all the synchronizable methods with an arbitrary number of parameters, but with only one line of code in the body. We also set the same zero-to-infinity limitation for the $statement$ variable in order to correct this.
