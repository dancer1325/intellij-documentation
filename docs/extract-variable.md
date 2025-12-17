[//]: # (Source: https://www.jetbrains.com/help/idea/extract-variable.html)
[//]: # (Downloaded: 2025-12-17 19:26:39)

## Example

Let's extract the `anotherClass.inValue()` variable that occurs twice throughout the code and give it a name `number`.

Before| After  
---|---  
public void method() { int a = 1; ... int b = a + anotherClass.intValue(); int c = b + anotherClass.intValue(); } |  public void method() { int a = 1; ... int number = anotherClass.intValue(); int b = a + number; int c = b + number; }   
  
Before| After  
---|---  
func method() { val a = 1 val b = a + anotherClass!!.intValue() val c = b + anotherClass!!.intValue() } |  func method() { val a = 1 val number = anotherClass!!.intValue() val b = a + number val c = b + number } 
