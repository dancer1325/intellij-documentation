[//]: # (Source: https://www.jetbrains.com/help/idea/exploring-go-core-dumps.html)
[//]: # (Downloaded: 2025-12-17 19:26:00)

# Exploring Go core dumps

Sometimes when you debug a program, you need to examine the code execution flow and understand the current state of a program. Go core dump is a file that contains the memory dump of running processes and their status during the life of a program. You can debug core dumps when the program finished its execution or while it is still running.

You can create Go core dump files only on Linux machines. But you can view the dump files on any operating system that supports IntelliJ IDEA.

### Create a Go core dump file on Linux

  1. Open a terminal in the directory with the file .

  2. Set the `ulimit` parameter to `unlimited`: `ulimit -c unlimited`.

  3. Build the program by running `go build .` in the terminal. The `build` command creates a binary file in the current project folder (for example, awesomeProject).

  4. To create a core dump file, run `GOTRACEBACK=crash ./<binary_file_name>` (for example, `GOTRACEBACK=crash ./awesomeProject`). This command creates a core file in the current project folder.

![Create Go core dumps on Linux](https://resources.jetbrains.com/help/img/idea/2025.3/go_create_go_core_dump.png)



### View the dump log

  1. Navigate to Run | Open Core Dump.

  2. In the Executable field, specify a path to the binary file (for example, awesomeProject).

  3. In the Core Dump field, specify a path to the `core` file (for example, core).

  4. Click OK. In the Debug tool window, select a frame that you want to inspect.

![Open the Go core dump in IntelliJ IDEA](https://resources.jetbrains.com/help/img/idea/2025.3/go_open_go_core_dump.png)



### View the Go core dump in IntelliJ IDEA

  1. Open or create the Go Build configuration for the Go file.

  2. In the Environment field, click the folder (![The folder icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.nodes.folder.svg)).

  3. In the Environment Variables dialog, click the Add icon (![The Add icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)).

  4. Click the Name field and type `GOTRACEBACK`.

  5. Click the Value field and type `crash`.

  6. Save all changes and click OK.

  7. Run the program `Shift+F10`. The output for the program is displayed in the debugger window.

![View Go core dumps in IntelliJ IDEA](https://resources.jetbrains.com/help/img/idea/2025.3/go_gotraceback_crash.png)



26 May 2024

[Go run/debug configurations](go-plugin-run-debug-configurations.html)[Exploring Windows minidumps](exploring-windows-minidumps.html)
