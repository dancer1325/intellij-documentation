[//]: # (Source: https://www.jetbrains.com/help/idea/extract-method.html)
[//]: # (Downloaded: 2025-12-17 19:26:29)

## Example

Let's extract the `a+b` expression into a method (function for Kotlin), and replace duplicates .

Before| After  
---|---  
public void method() { int a=1; int b=2; int c=a+b; int d=a+c; } |  public void method() { int a=1; int b=2; int c=add(a,b); int d=add(a,c); } ... private int add(int a, int b) { return a+b; }   
  
Before| After  
---|---  
fun method(){ val a = 1 val b = 2 val c = a + b val d = a + b } |  fun method(){ val a = 1 val b = 2 val c = add(a, b) val d = add(a, b) } private fun add(a: Int, b: Int) = a + b 
