[//]: # (Source: https://www.jetbrains.com/help/idea/extract-parameter.html)
[//]: # (Downloaded: 2025-12-17 19:26:33)

## Extract parameter examples

When extracting a new parameter you can either introduce a parameter into the existing method or use the Delegate via overloading method option to save the original method and define a new method with your parameter.

Let's replace the string value `"Hello, World!"` in the method `generateText ()` with the new parameter `text`. The value `"Hello, World!"` is passed to the method in the updated method call `generateText("Hello, World!")`.

Before| After  
---|---  
public class HelloWorldPrinter { public static void print() { System.out.println(generateText()); } private static String generateText() { return "Hello, World!".toUpperCase(); } } |  public class HelloWorldPrinter { public static void print() { System.out.println(generateText("Hello, World!")); } private static String generateText(String text) { return text.toUpperCase(); } }   
  
Before| After  
---|---  
object HelloWorldPrinter { fun print() { println(generateText()) } private fun generateText(): String { return "Hello, World!".toUpperCase() } } |  object HelloWorldPrinter { fun print() { println(generateText("Hello, World!")) } private fun generateText(text: String): String { return text.toUpperCase() } }   
  
Now let's use Delegate via overloading method. In this case, a new overloading method is created and the new parameter is extracted in the definition of this method (the second of the `generateText()` methods). The signature of the existing `generateText()` method is not changed. However, the method itself has been modified. Now, it calls the new `generateText()` method and passes the value `"Hello, World!"` to it in this call. Note that the existing call of `generateText()` (in the method `print()`) is not changed.

Before| After  
---|---  
public class HelloWorldPrinter { public static void print() { System.out.println(generateText()); } private static String generateText() { return "Hello, World!".toUpperCase(); } } |  public class HelloWorldPrinter { public static void print() { System.out.println(generateText()); } private static String generateText() { return generateText("Hello, World!"); } private static String generateText(String text) { return text.toUpperCase(); } }   
  
Before| After  
---|---  
object HelloWorldPrinter { fun print() { println(generateText()) } private fun generateText(): String { return "Hello, World!".toUpperCase() } } |  // if you selected the "Introduce default value" option object HelloWorldPrinter { fun print() { println(generateText()) } private fun generateText(text: String = "Hello, World!"): String { return text.toUpperCase() } } 
