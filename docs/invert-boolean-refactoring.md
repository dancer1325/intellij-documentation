[//]: # (Source: https://www.jetbrains.com/help/idea/invert-boolean-refactoring.html)
[//]: # (Downloaded: 2025-12-17 19:30:05)

## Example

Before| After  
---|---  
private double a; ... public boolean method() { if (a > 15 && a < 100) { a = 5; return true; } return false; } |  private double a; ... public boolean method() { if (a > 15 && a < 100) { a = 5; return false; } return true; }   
boolean b = true; ... public double method() { ... b = false; ... } |  boolean b = false; ... public double method() { ... b = true; ... } 
