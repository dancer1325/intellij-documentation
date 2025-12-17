[//]: # (Source: https://www.jetbrains.com/help/idea/examining-suspended-program.html)
[//]: # (Downloaded: 2025-12-17 19:25:56)

## Examine frames

The state of the program is represented by frames. When the program is suspended, the current frame stack is displayed on the Frames tab of the Debug tool window. 

![Frames tab in the Debug tool window](https://resources.jetbrains.com/help/img/idea/2025.3/debug_examining_frames_tab.png)

A frame corresponds to an active method or function call. It stores the local variables of the called method or function, its arguments, and the code context that enables expression evaluation.

![Frames and threads are selected in the Frames tab](https://resources.jetbrains.com/help/img/idea/2025.3/debug_examining_frames_threads.png)

To better understand the concept of frames, let's look into what happens when a program is run. The execution of the program starts from the `main` method, which in turn calls other methods. Each of these methods may make additional method calls. The set of local variables and parameters for each method call is represented by a frame. 

Each time a method is called, a new frame is added to the top of the stack. When the execution of a method is complete, the corresponding frame is removed from the stack (in the last in, first out fashion).

When you select a frame, the corresponding file will open in a preview tab, which means that it will close when you navigate away from this frame. To open the file in a regular tab, double-click the frame.

To change this behavior, click Show Options Menu ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) on the toolbar of the Debug tool window, then select Open Files in Preview Tab.

Examining frames helps you understand why particular parameters were passed to a method and what the state of the caller was at the time of calling.

### Thread Statuses

Thread statuses are provided by Java to reflect what is currently happening to the thread:

Thread status| Description  
---|---  
MONITOR| The thread is waiting on a Java monitor.  
NOT_STARTED| The thread has not yet been started.  
RUNNING| The thread is active and running.  
SLEEPING| The thread is sleeping because `Thread.sleep()` or `JVM_Sleep()` was called.  
UNKNOWN| The thread status is unknown.  
WAIT| The thread is waiting after `Object.wait()` or `JVM_MonitorWait()` was called.  
ZOMBIE| The thread has completed execution.  
  
### Thread Icons

Icons near each thread indicate the status of the thread:

Icon| Description  
---|---  
![Current thread](https://resources.jetbrains.com/help/img/idea/2025.3/app.debugger.threadCurrent.svg)| The current thread in suspended state.  
![Running thread](https://resources.jetbrains.com/help/img/idea/2025.3/app.debugger.threadRunning.svg)| An active thread.  
![Thread at breakpoint](https://resources.jetbrains.com/help/img/idea/2025.3/app.debugger.threadAtBreakpoint.svg)| The thread that has hit the current breakpoint.  
![Suspended thread](https://resources.jetbrains.com/help/img/idea/2025.3/app.debugger.threadSuspended.svg)| A suspended thread. Threads are marked as suspended when they were paused by the debugger.  
![Frozen thread](https://resources.jetbrains.com/help/img/idea/2025.3/app.debugger.threadFrozen.svg)| A frozen thread. Threads are marked as frozen when they were [manually paused](starting-the-debugger-session.html#pause-resume).  
  
For capturing threads, virtual threads, and Kotlin coroutines in text format, refer to [Thread dumps](thread-dumps.html).

By default, IntelliJ IDEA hides the frames that correspond to framework and library calls.

### Show frames from libraries

  * To reveal the hidden frames, press the Show All Frames toggle button ![show Frames from Libraries button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.filter.svg) located in the top-right corner of the Frames pane.

![Frames pane with 57 collapsed framework calls and Show All Frames button in the top-right corner](https://resources.jetbrains.com/help/img/idea/2025.3/show-frames-ij.png)



### Configure packages to hide

  1. Go to Settings `Ctrl+Alt+S` | Build, Execution, Deployment | Debugger | Stepping.

  2. Specify the packages that you want to hide under Do not step into classes.

  3. Make sure the Hide stack frames using stepping filters is enabled.




### Copy stack to clipboard

  * To copy the call stack for the current thread, right-click anywhere on the Frames tab and select Copy Stack.




### Export threads

If you need to get a report containing the state of each thread and its stack trace, use the Export Threads option. This is useful when you need to share the information about the threads in text format.

  1. Right-click anywhere on the Frames pane and select Export Threads from the menu.

![Export Threads menu item](https://resources.jetbrains.com/help/img/idea/2025.3/debug_examining_export_threads_1.png)
  2. To save a report as a text file, specify the path to the file in the Export Threads dialog and click Save, or click Copy to copy it to the clipboard.

![Export Preview dialog](https://resources.jetbrains.com/help/img/idea/2025.3/debug_examining_export_threads_2.png)


