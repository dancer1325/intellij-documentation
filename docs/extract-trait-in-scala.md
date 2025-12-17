[//]: # (Source: https://www.jetbrains.com/help/idea/extract-trait-in-scala.html)
[//]: # (Downloaded: 2025-12-17 19:26:36)

## Example

Let's create a class `Calculator` with several methods and extract one of the methods (`mul`) into a trait.

class Calculator { def add(a: Int, b: Int): Int = a + b def mul(a: Int, b: Int): Int = a match { case 0 =>0 case _ => add(b, mul(a-1, b)) } } 

trait Multiplier { this: Calculator => def mul(a: Int, b: Int): Int = a match { case 0 => 0 case _ => add(b, mul(a - 1, b)) } } 

class Calculator extends Multiplier { def add(a: Int, b: Int): Int = a + b } 

IntelliJ IDEA creates a new trait `Multiplier` that contains the `mul` method with its definition body. The class `Calculator` extends the trait `Multiplier`.
