[//]: # (Source: https://www.jetbrains.com/help/idea/convert-anonymous-to-inner.html)
[//]: # (Downloaded: 2025-12-17 19:22:31)

## Example

Before| After  
---|---  
public class Class { public Interface method() { final int i = 0; return new Interface() { public int publicMethod() { return i; } }; } } |  public class Class { public Interface method() { final int i = 0; return new MyInterfaceClass(i); } private static class MyInterfaceClass implements Interface { private final int i; public MyInterfaceClass(int i) { this.i = i; } public int publicMethod() { return i; } } } 
