[//]: # (Source: https://www.jetbrains.com/help/idea/find-and-replace-code-duplicates.html)
[//]: # (Downloaded: 2025-12-17 19:26:57)

## Example

Before| After  
---|---  
public void method() { int a = 1; int b = 2; int c = a+b; int d = b+c; } ... private int add(int a, int b) { return a+b; } |  public void method() { int a = 1; int b = 2; int c = add(a,b); int d = add(b,c); } ... private int add(int a, int b) { return a+b; } 
