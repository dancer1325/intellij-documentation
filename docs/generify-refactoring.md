[//]: # (Source: https://www.jetbrains.com/help/idea/generify-refactoring.html)
[//]: # (Downloaded: 2025-12-17 19:27:50)

## Example

IntelliJ IDEA tries to generate code, which is as correct as possible from the Java point of view. In other words, each context introduces some type restrictions, and the refactoring produces the best possible type (in our case `<String>`) that does not contradict with the existing contexts.

Before| After  
---|---  
public void method() { List list = new LinkedList(); list.add("string"); } |  public void method() { List<String> list = new LinkedList<String>(); list.add("string"); } 
