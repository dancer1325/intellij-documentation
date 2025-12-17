[//]: # (Source: https://www.jetbrains.com/help/idea/replace-constructor-with-factory-method.html)
[//]: # (Downloaded: 2025-12-17 19:57:34)

## Example

Before| After  
---|---  
// File Class.java public class Class { public Class(String s) { ... } } // File AnotherClass.java public class AnotherClass { public void method() { Class aClass = new Class("string"); } } |  // File Class.java public class Class { private Class(String s) { ... } public static Class createClass(String s) { return new Class(s); } } // File AnotherClass.java public class AnotherClass { public void method() { Class aClass = Class.createClass("string"); } } 
