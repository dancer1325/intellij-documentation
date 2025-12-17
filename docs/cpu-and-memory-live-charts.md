[//]: # (Source: https://www.jetbrains.com/help/idea/cpu-and-memory-live-charts.html)
[//]: # (Downloaded: 2025-12-17 19:22:41)

# CPU and memory live charts

IntelliJ IDEA provides a way to monitor live performance statistics for a running process through CPU and Memory Live Charts.

As opposed to viewing static figures, live data may help you to visualize resource consumption, identify resource-related bottlenecks, and understand how certain events affect the program performance.

For example, in the picture below, we can see what a memory leak looks like in the Heap Memory chart. Sometimes it is enough to figure out the cause, and when it is not enough, it can give a clue for further investigation.

![Memory leak on CPU and Memory Live Charts](https://resources.jetbrains.com/help/img/idea/2025.3/cpu-memory-charts-leak.png)

CPU and Memory Live Charts are automatically shown for the following [run/debug configurations](run-debug-configuration.html):

  * [Application](run-debug-configuration-java-application.html) (Java/Kotlin)

  * [JUnit](run-debug-configuration-junit.html), [TestNG](run-debug-configuration-testng.html)

  * [Maven](run-debug-configuration-maven.html)

  * [JAR](run-debug-configuration-jar.html)

  * [Spring Boot](run-debug-configuration-spring-boot.html), [Quarkus](quarkus-run-configuration.html), 

[Micronaut](micronaut.html), 

[Ktor](ktor.html)

  * [Shell script](run-debug-configuration-shell-script.html)


![CPU and Memory Live Charts in the Run tool window](https://resources.jetbrains.com/help/img/idea/2025.3/cpu-memory-live-charts-in-run.png)

### Open CPU and Memory Live Charts for an arbitrary Java process

In case the target process was launched outside IntelliJ IDEA, you can open CPU and Memory Live Charts from the Profiler home page. This dedicated view will also show thread usage data.

  1. In the main menu, go to View | Tool Windows | Profiler.

  2. Right-click the necessary process in the Profiler tool window and select CPU and Memory Live Charts.

![Accessing live charts for a running process](https://resources.jetbrains.com/help/img/idea/2025.3/cpu-memory-live-charts.png)

A new tab opens in which you can see the resources the selected process consumes.

![CPU and Memory live charts](https://resources.jetbrains.com/help/img/idea/2025.3/cpu-memory-chart.png)



The following metrics are available:

  * CPU – CPU load for the given process. Each process has its own figure.

  * Heap memory – the current usage of [heap memory](https://docs.oracle.com/javase/specs/jvms/se17/html/jvms-2.html#jvms-2.5.3) and maximum heap size. The heap size increases when new [objects of reference types](https://docs.oracle.com/javase/specs/jvms/se17/html/jvms-2.html#jvms-2.4) are allocated and decreases when they are garbage-collected.

  * Threads – the overall number of [threads](https://docs.oracle.com/javase/specs/jls/se17/html/jls-17.html) (yellow) and daemon threads (red). The number after the slash is the peak number of threads since the process has started.

  * Non-heap memory – this type of memory is used by the JVM to store class metadata, method data, and other JVM internals. The first value is the current memory value, and the second is the maximum value since the charts have started.




### Get a metric for a specific instant

  * Hover over the point on the chart. IntelliJ IDEA will show the corresponding metric and timestamp.

![The numeric value appears on hovering over the chart](https://resources.jetbrains.com/help/img/idea/2025.3/cpu-memory-charts-point.png)



### Adjust the timeframe

  * Click ![The Presentation Settings button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.inspectionsEye.svg) and select the time period over which you want to see the collected data. Alternatively, you can select Show all data – this will display the entire recording.

![The options in the Presentation Settings menu allowing you to change the inspected timeframe](https://resources.jetbrains.com/help/img/idea/2025.3/charts-timeframe.png)



### Call garbage collection

  * If you need to test how garbage collection works under specific conditions, you can request it from CPU and Memory Live Charts. For that, click the Perform GC button.

![Perform GC button](https://resources.jetbrains.com/help/img/idea/2025.3/gc-1.png)



29 July 2025

[Introduction to profiling](profiler-intro.html)[Introduction to CPU and allocation profiling](cpu-and-allocation-profiling-basic-concepts.html)
