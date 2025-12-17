[//]: # (Source: https://www.jetbrains.com/help/idea/extract-field.html)
[//]: # (Downloaded: 2025-12-17 19:26:19)

## Example

Let's extract the `anotherClass.intValue();` variable into a field. As a result, IntelliJ IDEA changes the selected variable name to `number` and declares it as the `private int number` field.

Before| After  
---|---  
public class Class { AnotherClass anotherClass; public void method() { int a = 1; int b = a + anotherClass.intValue(); int c = b + anotherClass.intValue(); } } |  public class Class { public AnotherClass anotherClass; private int number; public void method() { int a = 1; number = anotherClass.intValue(); int b = a + number; int c = b + number; } } 
