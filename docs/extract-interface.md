[//]: # (Source: https://www.jetbrains.com/help/idea/extract-interface.html)
[//]: # (Downloaded: 2025-12-17 19:26:23)

## Examples

Here we have a class and perform the Extract Interface refactoring to create an interface based on the methods of the class.

Before| After  
---|---  
// File AClass.java class AClass { public static final double CONSTANT = 3.14; public void publicMethod() { } public void secretMethod() { } } |  // File AClass.java class AClass implements AnInterface { public void publicMethod() { } public void secretMethod() { } // File AnInterface.java public interface AnInterface { double CONSTANT = 3.14; void publicMethod(); } }   
  
Another example of the Extract Interface refactoring, when the Rename original class and use interface where possible option is selected.

Before| After  
---|---  
public class FormerAClass implements AClass { public void publicMethod() { } public void secretMethod() { } } |  public interface AClass { double CONSTANT=3.14; void publicMethod(); }   
  
You can extract an interface from the class that already implements another interface. Let's extract interface from the class that implements `AnInterface`. Depending on whether we want `AnotherInterface` (extracted interface) to extend the `AnInterface` (existing one) or we want source `AClass` to implement them both, we will get the following code:

Extracted Interface extends the existing one:

class AClass implements AnotherInterface { public void publicMethod() { //some code here } public void secretMethod() { //some code here } } 

Extracted Interface:

public interface AnotherInterface extends AnInterface { } 

Source class implements both interfaces.

Source class:

class AClass implements AnInterface, AnotherInterface { public void publicMethod() { //some code here } public void secretMethod() { //some code here } } 

Extracted Interface:

public interface AnotherInterface { } 
