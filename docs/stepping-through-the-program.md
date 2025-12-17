[//]: # (Source: https://www.jetbrains.com/help/idea/stepping-through-the-program.html)
[//]: # (Downloaded: 2025-12-17 20:03:23)

## Step over

Steps over the current line of code and takes you to the next line even if the highlighted line has method calls in it. The implementation of the methods is skipped, and you move straight to the next line of the caller method.

public static void main(String[] args) { // the program is suspended here count(10); System.out.printIn("Count complete!"); } 

In the example, line 5 is about to be executed. If you step over, the debugger will move straight to line 6 without visiting the `count()` method.

public static void main(String[] args) { count(10); // execution point moves here after Step Over System.out.printIn("Count complete!"); } 

If there are breakpoints inside the skipped methods, the debugger will stop at them. To skip any breakpoints on the way, use [Force step over](#force-step-over). 
