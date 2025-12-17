[//]: # (Source: https://www.jetbrains.com/help/idea/replace-inheritance-with-delegation.html)
[//]: # (Downloaded: 2025-12-17 19:57:35)

## Example

Before| After  
---|---  
// File Class.java public class Class extends SuperClass { public int varInt; public void openMethod() { ... } } // File SuperClass.java public abstract class SuperClass { public static final int CONSTANT=0; public abstract void openMethod(); public void secretMethod() { ... } } |  // File Class.java public class Class { public int varInt; private final MySuperClass superClass = new MySuperClass(); public SuperClass getSuperClass() { return superClass; } public void openMethod() { superClass.openMethod(); } private class MySuperClass extends SuperClass { public void openMethod() { ... } } } // File SuperClass.java UNCHANGED public abstract class SuperClass { public static final int CONSTANT=0; public abstract void openMethod(); public void secretMethod() { ... } } 
