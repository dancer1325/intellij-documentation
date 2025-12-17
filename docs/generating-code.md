[//]: # (Source: https://www.jetbrains.com/help/idea/generating-code.html)
[//]: # (Downloaded: 2025-12-17 19:27:41)

## Generate constructors

IntelliJ IDEA can generate a constructor that initializes specific class fields using values of corresponding arguments.

### Generate a constructor for a class

  1. In the main menu, go to Code and select Generate (`Alt+Insert`).

  2. In the Generate popup, click Constructor.

  3. If the class contains fields, select the fields to be initialized by the constructor and click OK.




The following code fragment shows the result of generating a constructor for a class:

public class MyClass { int aInteger; double bDouble; public MyClass(int myAIntegerParam, double myBDoubleParam) { aInteger = myAIntegerParam; bDouble = myBDoubleParam; } } 
