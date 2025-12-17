[//]: # (Source: https://www.jetbrains.com/help/idea/using-breakpoints.html)
[//]: # (Downloaded: 2025-12-17 20:05:19)

## Types of breakpoints

The following types of breakpoints are available in IntelliJ IDEA:

  * Line breakpoints: suspend the program upon reaching the line of code where the breakpoint was set. This type of breakpoints can be set on any executable line of code.

  * Method breakpoints: suspend the program upon entering or exiting the specified method or one of its implementations, allowing you to check the method's entry/exit conditions.

  * Field watchpoints: suspend the program when the specified field is read or written to. This allows you to react to interactions with specific instance variables. For example, if at the end of a complicated process you are ending up with an obviously wrong value on one of your fields, setting a field watchpoint may help determine the origin of the fault.

Field watchpoints do not work for field modifications made through reflection.

  * Exception breakpoints: suspend the program when `Throwable` or its subclasses are thrown. They apply globally to the exception condition and do not require a particular source code reference. Unlike stack traces, suspending an application on an exception allows you to examine the surrounding context or data while it is still available. 



