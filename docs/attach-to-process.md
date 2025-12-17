[//]: # (Source: https://www.jetbrains.com/help/idea/attach-to-process.html)
[//]: # (Downloaded: 2025-12-17 19:18:34)

## Prerequisites

While not absolutely required to attach, the following prerequisites have to be met to enable full-fledged debugging:

  * The remote process should be started with the [debug agent](#debug-agent).

  * The application needs to be compiled with [debugging information](#debug-info).

  * You need to have the [application's source code](#sources).




Debugging is still possible even when none of these are met, however, there are limitations associated with each of them. These requirements are described in more detail in subsequent chapters.

### Debug agent

Processes intended to allow debugger connections are started with the debug agent. Debug agent is a component of a host application that is responsible for communicating with the debugger. The communication happens over a socket connection, irrespective of whether the process is local or remote.

### Start a process with the debug agent

  * When starting the process, add the following line to its VM options:

-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=*:5005 

The option has the following parameters:

    * `address` – the port that will be used for debugging

    * `server=y` – specifies that the process should listen for incoming debugger connections (act as a server).

    * `suspend` – specifies whether the VM should wait until the debugger has connected or start executing the application's code immediately

-agentlib:jdwp=transport=dt_socket,server=n,address=192.168.1.178:5005,suspend=y,onthrow=<FQ exception class name>,onuncaught=<y/n>

The option has the following parameters:

    * `address` – the IP address and the port of the server end. Both IPv4 and IPv6 are supported.

    * `server=n` – specifies that the process should connect to the debugger (act as a client)

    * `suspend=y` – specifies that the VM should wait until the debugger has connected before executing the application code.

    * `onthrow` – optionally delays the connection until the specified exception is thrown. Use the exception's fully-qualified name as the value.

    * `onuncaught` – optionally delays the connection until an uncaught exception is thrown. Use the exception's fully-qualified name as the value.

The format may differ depending on the JDK version. To get an appropriately formatted string for your JDK, you can select the required JDK version in the [Remote JVM debug](#create-rc) run/debug configuration and copy it from there. 




If the process is launched through another process, for example, a web container like Apache Tomcat, the debug agent VM option may need to be specified indirectly. For example, the other process may use a configuration file for passing the option to the host VM. In case of popular web servers and frameworks, IntelliJ IDEA provides [run/debug configurations](list-of-run-debug-configurations.html) that do this for you.

### Add IntelliJ IDEA's debug agent

You can use advanced IntelliJ IDEA's functionality, such as [Async stack traces](debug-asynchronous-code.html), when debugging a process launched outside IntelliJ IDEA. For this you need to load the IntelliJ IDEA's debug agent to the process.

  * Add debugger-agent.jar from IntelliJ IDEA's installation directory using the `javaagent` VM option. For example:

java -agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=\\*:5005 -javaagent:"/Users/me.user/Applications/IntelliJ IDEA Ultimate 2024.3.app/Contents/plugins/java/lib/rt/debugger-agent.jar" Alphabet 




If a local process doesn't use the debug agent, you can still attach to it in the read-only mode. The debugger functionality will be limited to viewing the call stack and examining the related local variables.

An example of the situation when it can be useful is when your program hung while batch-processing some files. Using the read-only mode, you can figure out what method caused the program to hang, and which file it is processing at the moment.

### Debug information

Debug information is a special kind of information in the application bytecode. The debugger uses this information to identify local variables, line numbers, and so on. The bytecode of an application may or may not have debugging information included.

The debug information is provided to the program at compile-time. This is controlled with the `-g` compiler flag. By default, the compiler includes most of the information required for debugging, but if it was not you, who compiled the application, it may happen that the program that you are going to debug was compiled without this information.

If the bytecode of the application does not include debug information, the debugger will still be able to attach, however, some of the debugger functionality may be unavailable. For example, it is not possible to view line numbers or stop at breakpoints without line number information:

![debug_line_numbers_unavailable.png](https://resources.jetbrains.com/help/img/idea/2025.3/debug_line_numbers_unavailable.png)

The bare minimum that is always available regardless of whether the debug information is present:

  * Class names, unless the code is obfuscated

  * Static and instance variables

  * Call stack




For more information about configuring debug info generation, refer to [Java compiler documentation](https://docs.oracle.com/javase/7/docs/technotes/tools/windows/javac.html).

### Application sources

It is recommended that you have the access to the sources of the project you are debugging. IntelliJ IDEA matches debugging events with the sources and displays information relevant to the debugging session in the editor. This allows you to view the debugging session as if it was the source code that is being executed.

![debug_in_editor.png](https://resources.jetbrains.com/help/img/idea/2025.3/debug_in_editor.png)

For IntelliJ IDEA to find the source files, they must be included in the classpath.
