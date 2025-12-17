[//]: # (Source: https://www.jetbrains.com/help/idea/analyzing-data-flow.html)
[//]: # (Downloaded: 2025-12-17 19:18:10)

## Analyze stack traces

When your program crashes with an exception, you can use the stack trace as the input for data flow analysis. This helps you track where inappropriate values may come from.

public class ArrayTest { static int[] ints = new int[5]; public static void main(String[] args) { ArrayTest arrayTest = new ArrayTest(); int a = arrayTest.getRandomElement(ints); System.out.println(a); } private int getRandomElement(int[] array) { int index = new java.util.Random().nextInt(20); return array[index]; } } 

The code above creates a fixed-size array and tries to access a random element from it. Sometimes it throws an `ArrayOutOfBoundsException` because the index may be greater than the length of the array.

  1. In the stack trace, click the source reference of the frame that threw the exception.

![Stack trace](https://resources.jetbrains.com/help/img/idea/2025.3/dfa_stacktrace.png)

The editor takes you to the corresponding line in the source.

  2. Click the popup to find the source of the value that caused the exception.

![Stack trace](https://resources.jetbrains.com/help/img/idea/2025.3/dfa_stacktrace_2.png)



Dataflow to here opens with the filters applied.
