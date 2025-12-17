[//]: # (Source: https://www.jetbrains.com/help/idea/debug-your-first-kotlin-application.html)
[//]: # (Downloaded: 2025-12-17 19:24:19)

## What Is Debugging?

Broadly, debugging is the process of detecting and correcting errors in a program.

There are different kinds of errors, which you are going to deal with. Some of them are easy to catch, like syntax errors, because they are taken care of by the compiler. Another easy case is when the error can be quickly identified by looking at the stack trace, which helps you figure out the cause.

However, there are errors that can be very tricky and take really long to find and fix. For example, a subtle logic error, which happened early in the program may not manifest itself until very late, making it a real challenge to sort things out.

This is where the debugger is useful. It is a tool that lets you find bugs in an efficient manner by providing an insight into the internal operations of a program. This is possible by pausing the execution at a specified point, analyzing the program state, and, if necessary, advancing the execution step-by-step. While debugging, you are in full control of the things. In this manual we are covering a basic debugging scenario to get you started.
