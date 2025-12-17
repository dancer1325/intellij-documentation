[//]: # (Source: https://www.jetbrains.com/help/idea/change-signature.html)
[//]: # (Downloaded: 2025-12-17 19:19:48)

## Change Class Signature example

Let's add type parameters `Param1, Param2` to a class `MyClass`.

For [Kotlin](https://kotlinlang.org/docs/reference/), this refactoring works the same as for Java. You can press `Ctrl+Alt+Shift+K` to convert your Java code to Kotlin.

String and Integer are default values that were specified in the Change Class Signature dialog for `Param1` and `Param2` respectively.

You can also add a bounded value for a parameter to put some restrictions on what gets passed to the type parameter. For example, add `Param3` with default value `List` and bounded value `Collection`

![Change a class signature](https://resources.jetbrains.com/help/img/idea/2025.3/change_class_signature.png)

Before| After  
---|---  
public class MyClass { public class MyOtherClass { MyClass myClass; void myMethod(MyClass myClass) { } } } |  public class MyClass<Param1, Param2, Param3 extends Collection> { public class MyOtherClass { MyClass<String, Integer> myClass; void myMethod(MyClass<String, Integer, List> myClass) { } } }   
  
The refactoring may be useful for changing the parameter order in the class signature as well as in all its usages.
