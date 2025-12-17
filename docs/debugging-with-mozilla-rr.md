[//]: # (Source: https://www.jetbrains.com/help/idea/debugging-with-mozilla-rr.html)
[//]: # (Downloaded: 2025-12-17 19:24:26)

# Debugging with Mozilla rr

Mozilla rr is a tool that you can use to record, replay, and debug applications. The main idea of Mozilla rr is to help you catch non-trivial bugs.

Mozilla rr records the whole program execution. It means that you can debug the recorded trace only when the program ends its execution. For servers and other long-running applications, you must terminate the running application (for example, by sending the SIGTERM signal from the console). After the recording, you can replay the execution in the debugger as many times as you need. Read more about Mozilla rr on the [official Mozilla rr site](https://rr-project.org/).

### Debug code with Mozilla rr

  1. Install Mozilla rr. For installation instructions, refer to the [Building And Installing](https://github.com/mozilla/rr/wiki/Building-And-Installing).

  2. In IntelliJ IDEA, set a breakpoint. To set a breakpoint, click the gutter near the code line where you want the debugger to stop code execution. For more information about breakpoints, refer to [Debug code](debugging-code.html) and [Breakpoints](using-breakpoints.html).

  3. Click the Run icon (![The Run icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.runConfigurations.testState.run.svg)) in the gutter and select Record and Debug <configuration_name>. In the Debugger tool window, you can see a status of variables, processes, and threads on different stages of code execution.


![Debug code with Mozilla rr](https://resources.jetbrains.com/help/img/idea/2025.3/go_navigate_through_trace.png)

### Navigate through the recorded trace

  1. Navigate to Run | Debug Saved Trace.

  2. In the Trace directory field, specify a path to the trace directory.

  3. Click OK.

  4. In the Debugger tool window, click the Resume Program icon ![The Resume Program icon ](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.resume_dark.svg) to continue program execution, or click the Rewind icon below to run the debug session backwards until the previous breakpoint.


![Navigate through the recorded trace](https://resources.jetbrains.com/help/img/idea/2025.3/go_navigate_controls.png)

### Collecting Mozilla rr traces

  1. Build an executable by using the Go build run/debug configuration. To easily find the executable, specify the current project directory in the Output directory field of the Go build configuration. 

  2. Open the terminal and run the following Mozilla rr command: `rr record <path_to_the_application_executable>`

As a result, the Mozilla rr trace files appear in the following folder: ~/.local/share/rr/<executable_name>

![Collecting Mozilla rr traces](https://resources.jetbrains.com/help/img/idea/2025.3/go_collect_mozilla_rr_trace.png)



### Remote debugging with Mozilla rr

  1. On the remote machine, [collect the Mozilla rr trace](#collecting-mozilla-rr-traces).

  2. On the remote machine, start the debugger by opening the terminal and running the following command: `dlv --headless --api-version=2 -l localhost:2345 replay /path/to/trace/dir /path/to/binary`

  3. On the local machine, create the Go Remote run/debug configuration. In the Go Remote configuration, specify the remote machine IP address and port.

  4. On the local machine, ensure that the Go Remote run/debug configuration is selected from the list of configurations.

  5. On the local machine, click Run | Debug <remote_configuration_name>. Alternatively, press `Shift+F9`.

![Remote debugging with Mozilla rr](https://resources.jetbrains.com/help/img/idea/2025.3/go_remote_debug_with_mozilla_rr.png)



07 August 2025

[Exploring Windows minidumps](exploring-windows-minidumps.html)[Using profiler labels](using-profiler-labels.html)
