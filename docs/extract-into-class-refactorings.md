[//]: # (Source: https://www.jetbrains.com/help/idea/extract-into-class-refactorings.html)
[//]: # (Downloaded: 2025-12-17 19:26:24)

## Extract delegate example

The Extract Delegate refactoring lets you extract some of the fields and methods of a class into a separate, newly created class.

The Extract Delegate refactoring can also be accessed from a [UML Class diagram](class-diagram.html).

Before| After  
---|---  
public class Foo { private String b; public String getInfo() { return ("(" + b + ")"); } ... } public class Bar { Foo foo; String t2 = foo.getInfo(); ... } |  public class Foo { private final Info info = new Info(); public String getInfo() { return info.getInfo(); } ... } public class Info { private String b; public Info() {} public String getInfo() { return ("(" + b + ")"); } } public class Bar { Foo foo; String t2 = foo.getInfo(); ... } 
