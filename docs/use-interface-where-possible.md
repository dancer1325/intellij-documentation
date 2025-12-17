[//]: # (Source: https://www.jetbrains.com/help/idea/use-interface-where-possible.html)
[//]: # (Downloaded: 2025-12-17 20:05:14)

## Example

Before| After  
---|---  
// File Class.java public class Class implements Interface { public void publicMethod() { ... } public void hiddenMethod() { ... } } |  // File Class.java UNCHANGED public class Class implements Interface { public void publicMethod() { ... } public void hiddenMethod() { ... } }   
// File Interface.java public interface Interface { int CONSTANT=0; void publicMethod(); } |  // File Interface.java UNCHANGED public interface Interface { int CONSTANT=0; void publicMethod(); }   
// File AnotherClass.java public class AnotherClass { Class firstClass; Class secondClass; public void method() { firstClass.publicMethod(); firstClass.hiddenMethod(); secondClass.publicMethod(); if (secondClass instanceof Class) { ... } ... } } |  // File AnotherClass.java MODIFIED public class AnotherClass { Class firstClass; Interface secondInterface; public void method() { firstClass.publicMethod(); firstClass.hiddenMethod(); secondInterface.publicMethod(); if (secondInterface instanceof Interface) { ... } ... } } 
