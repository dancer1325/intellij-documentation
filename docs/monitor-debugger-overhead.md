[//]: # (Source: https://www.jetbrains.com/help/idea/monitor-debugger-overhead.html)
[//]: # (Downloaded: 2025-12-17 19:32:36)

## Optimize conditional breakpoints

Breakpoints that use conditions can cause significant overhead when hit too frequently.

When this happens, you can substitute the conditional breakpoint with an `if` statement and a regular breakpoint inside.

// hot loop for (int i = 0; i < Integer.MAX_VALUE; i++) { System.out.println("some code"); if (breakpointCondition) { System.out.println("Set breakpoint here"); } } 

Conditions in code are evaluated much faster, which can significantly improve the performance of the debugged application.
