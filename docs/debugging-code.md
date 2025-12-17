[//]: # (Source: https://www.jetbrains.com/help/idea/debugging-code.html)
[//]: # (Downloaded: 2025-12-17 19:24:20)

## General debugging procedure

There is no one-size-fits-all procedure for debugging applications. Depending on actual requirements, you may have to use different actions in a different order. This topic provides general guidelines, which represent typical debugging steps. The details on how and when to use particular features are provided in the respective topics. 

  1. Define where the program needs to be stopped. This is done using [breakpoints](using-breakpoints.html). Breakpoints are special markers, which represent places and conditions when the debugger needs to step in and freeze the program state. A program, which has been frozen by the debugger is referred to as suspended.

The alternative to using breakpoints is [manually suspending](starting-the-debugger-session.html) the program at an arbitrary moment, however this method imposes some limitations on the debugger functionality and doesn't allow for much precision as to when to suspend the program.

  2. [Run your program in debug mode](starting-the-debugger-session.html). This might be a regular application, a unit test, or any other executable code, as long as the corresponding run configuration supports debugging. 

Just like with regular running of the program, you can run multiple debugging sessions at the same time.

  3. After the program has been suspended, use the debugger to [get the information about the state of the program](examining-suspended-program.html) and how it changes during running.

The debugger provides you with the information about variable values, the current state of the threads, breakdown of objects that are currently in the heap, and so on. It also allows you to test your program in various conditions by throwing exceptions (for example, to check how they are handled) or running arbitrary code right in the middle of the program execution. 

While these tools let you examine the program state at a particular instant, the [stepping](stepping-through-the-program.html) feature gives you the control over step-by-step execution of the program. By combining the tools you can deduce where the bug is coming from and test your program for robustness.

  4. When you have determined what needs to be fixed, you can do it without terminating the session. For this purpose, IntelliJ IDEA provides a functionality allowing you to adjust and reload pieces of your code on the fly. This approach is covered in the [Reload modified classes](altering-the-program-s-execution-flow.html#reload_classes) topic. 




If you are new to debugging, we recommend that you complete the [Debugging Your First Java Application](debugging-your-first-java-application.html) tutorial.
