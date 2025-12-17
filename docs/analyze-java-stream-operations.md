[//]: # (Source: https://www.jetbrains.com/help/idea/analyze-java-stream-operations.html)
[//]: # (Downloaded: 2025-12-17 19:18:07)

# Analyze Java Stream operations

Java Streams may sometimes be difficult to debug. This happens because they handle the processing logic behind the scenes, and it might complicate tracing how particular values are derived. To help you debug Java Streams, IntelliJ IDEA lets you visualize what is going on in a Java Stream.

This feature is only available for project files. Java Stream debugger doesn't work with libraries or decompiled code.

Let's take a simple program written in functional style to demonstrate how the feature works.

import java.util.stream.IntStream; class PrimeFinder { static int skip = 0; static int limit = 100; public static void main(String[] args) { if (args.length >= 1) skip = Integer.parseInt(args[0]); if (args.length >= 2) limit = Integer.parseInt(args[1]); IntStream.iterate(1, n -> n + 1) .skip(skip) .limit(limit) .filter(PrimeTest::isPrime) .forEach(System.out::println); } } class PrimeTest { static boolean isPrime(int candidate) { return candidate == 91 || // a bug here IntStream.rangeClosed(2, (int) Math.sqrt(candidate)) .noneMatch(n -> (candidate % n == 0)); } } 

As the classes' names suggest, the app finds prime numbers. You can specify the starting number and the number of candidates to check using the program arguments. The checking logic is handled by a Java 8 Stream.

Now if we look at the program output, we see extra numbers there.

79 83 89 91 <\- extra 97 

To understand where these incorrect numbers are coming from, let's use the stream debugger feature.

  1. Suspend the program at a line where the stream is used. You can use any stream operation for this including terminal ones.

public static void main(String[] args) { if (args.length >= 1) skip = Integer.parseInt(args[0]); if (args.length >= 2) limit = Integer.parseInt(args[1]); IntStream.iterate(1, n -> n + 1) // set breakpoint here .skip(skip) .limit(limit) .filter(PrimeTest::isPrime) .forEach(System.out::println); } 

  2. In the Debug tool window's toolbar, click More ![More button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.moreVertical.svg) then select Trace Current Stream Chain ![Trace Current Stream Chain button](https://resources.jetbrains.com/help/img/idea/2025.3/java-debugger-streams.icons.stream_debugger.svg).

  3. Use the Stream Trace dialog to analyze the operations inside the stream. The tabs in the top part let you switch between particular operations and see how the values are transformed with each operation.

![The Stream Trace dialog](https://resources.jetbrains.com/help/img/idea/2025.3/debug_analyze_streams_2.png)

To get a bird's eye view of all transformations at once, click Flat Mode. Terminal operations without a return value like `forEach` are not displayed in the Flat Mode.




The examination of the stream shows that the extra value is coming from the `filter` operation. The search of a bug is now narrowed down to the `Predicate` of `filter`, or more specifically, `PrimeTest.isPrime()` method.

Stream trace does not reach beyond the terminal operation of a stream. This means that if there is further chaining, for example with `Optional`, it will not be visible from the Stream Trace dialog.

08 May 2025

[Analyze objects in the JVM heap](analyze-objects-in-the-jvm-heap.html)[Debug asynchronous code](debug-asynchronous-code.html)
