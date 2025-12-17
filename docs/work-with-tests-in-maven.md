[//]: # (Source: https://www.jetbrains.com/help/idea/work-with-tests-in-maven.html)
[//]: # (Downloaded: 2025-12-17 20:07:16)

## Debug tests with Maven

You can debug tests executed by Maven. For example, if you want to debug tests running in a pipeline, then you can fork the process and debug it remotely using Maven commands.

For more information, refer to the [Maven documentation](https://maven.apache.org/surefire/maven-surefire-plugin/examples/debugging.html) and the [remote debugging](tutorial-remote-debug.html) process.

### Debug tests

  1. In your Maven project, open the Run/Debug Configurations dialog.

  2. Add a new Remote JVM Debug configuration.

  3. In the options on the right, add a name, change the port if needed (the default is `8000`), select the module classpath and click OK.

![Debug configurations](https://resources.jetbrains.com/help/img/idea/2025.3/mvn_debug_config.png)
  4. Set the [break points](using-breakpoints.html) where needed.

  5. Press `Ctrl` twice to open the [Run Anything](running-anything.html) window. Enter the [Maven command](https://maven.apache.org/surefire/maven-surefire-plugin/examples/debugging.html#forked-tests) for forked tests. The default 5005 port is used for the process. However, you can change the port and run it on the local host with the following command: 

mvn -Dmaven.surefire.debug="-agentlib:jdwp=transport=dt_socket,server=y,suspend=y,address=localhost:8000" test 

![Local terminal](https://resources.jetbrains.com/help/img/idea/2025.3/local_teminal_mvnDebug.png)

You can check what other [Maven commands](https://maven.apache.org/surefire/maven-surefire-plugin/examples/debugging.html#non-forked-tests) can be used. For example, what to use if you don't want to fork the debugging process.

You can check the running process in the Run tool window.

![Run tool window](https://resources.jetbrains.com/help/img/idea/2025.3/run_tool_window_mvn.png)
  6. Start the debugging process, by clicking ![the Debug button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.startDebugger.svg) against the created debug configuration on the main toolbar.

Check the result in the Debug tool window.

![the Debug console tab](https://resources.jetbrains.com/help/img/idea/2025.3/debug_console.png)

As the code executes, it will pause at the breakpoints you have set in your code.



