[//]: # (Source: https://www.jetbrains.com/help/idea/convert-to-instance-method.html)
[//]: # (Downloaded: 2025-12-17 19:22:32)

## Example

Consider classes `MyClass`, `ClassB` and `ClassB` residing in the same package.

As a result, `MyClass` and `ClassB` become converted.

public class MyClass { ClassA classA = new ClassA(); ClassB classB = new ClassB(); static public void greatMethod(ClassA classA, ClassB classB){ System.out.println("classA = " + classA); System.out.println("classB = " + classB); } public void myMethod(){ MyClass.greatMethod(classA, classB); } } 

public class MyClass { ClassA classA = new ClassA(); ClassB classB = new ClassB(); public void myMethod(){ classB.greatMethod(classA); } } public class ClassB { public void greatMethod(ClassA classA) { System.out.println("classA = " + classA); System.out.println("classB = " + this); } } 
