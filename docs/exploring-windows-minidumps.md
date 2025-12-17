[//]: # (Source: https://www.jetbrains.com/help/idea/exploring-windows-minidumps.html)
[//]: # (Downloaded: 2025-12-17 19:26:02)

# Exploring Windows minidumps

You can create Windows minidumps only on the Microsoft Windows operating system. But you can analyze and debug your application on all supported operating systems.

Windows minidump files record the state of a program as it is running, or as at the moment of a crash. To read a minidump file, you must have the binaries of your application and the dump file.

### Create a binary file of your application

  1. Open the Run/Debug Configuration dialog in one of the following ways:

     * Select Run | Edit Configurations from the main menu.

     * With the [Navigation bar](guided-tour-around-the-user-interface.html#navigation-bar) visible (View | Appearance | Navigation Bar), choose Edit Configurations from the run/debug configuration selector. 

     * Press `Alt+Shift+F10` and then press `0`.

  2. In the [Run/Debug Configuration](run-debug-configurations-dialog.html) dialog, click the Add New Configuration icon (![the Add New Configuration icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)) on the toolbar or press `Alt+Insert`. The list shows the default run/debug configurations. Select the desired configuration type (for example, Go build).

The fields that appear in the right-hand pane display the default settings for the selected configuration type.

  3. In the Name field, type the configuration name.

  4. In the Files field, add the name of the file that you want to run (for example, main.go).

  5. In the Output Directory field, specify the path where you want to store the created binary file.

  6. Apply the changes and close the dialog.




### Create the minidump file on Windows

  1. Start the application and use it as usual.

You can run the generated EXE file or run the application from IntelliJ IDEA. To run the application from IntelliJ IDEA, click the Run icon ![The Run icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.execute.svg) in the gutter near the main function and select Run 'go build <configuration_name>'.

  2. Open the Windows Task Manager `Ctrl+Alt+Delete`, click the Processes tab.

  3. Right-click your application and select Create dump file.


![Create the minidump file on Windows](https://resources.jetbrains.com/help/img/idea/2025.3/go_create_minidump_on_windows.png)

### Open the minidump file in IntelliJ IDEA

  1. Navigate to Run | Open Core Dump.

  2. In the Executable field, specify a path to the EXE file.

  3. In the Core Dump field, specify a path to the dump file.

  4. Click OK.


![Open the minidump file in IntelliJ IDEA](https://resources.jetbrains.com/help/img/idea/2025.3/go_open_minidump_file.png)

03 September 2025

[Exploring Go core dumps](exploring-go-core-dumps.html)[Debugging with Mozilla rr](debugging-with-mozilla-rr.html)
