[//]: # (Source: https://www.jetbrains.com/help/idea/pull-members-up.html)
[//]: # (Downloaded: 2025-12-17 19:56:28)

## Pull Members Up example

Before| After  
---|---  
// File Class.java public class Class extends SuperClass { public void publicMethod() { } public void hiddenMethod() { } } // File SuperClass.java public abstract class SuperClass { public abstract void publicMethod(); } |  // File Class.java public class Class extends SuperClass { public void publicMethod() { } } // File SuperClass.java public abstract class SuperClass { public abstract void publicMethod(); public void hiddenMethod() { } } 
