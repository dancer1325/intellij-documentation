[//]: # (Source: https://www.jetbrains.com/help/idea/run-java-applications.html)
[//]: # (Downloaded: 2025-12-17 19:59:07)

# Tutorial: Run a Java application

This tutorial explains how to run a Java application, use run/debug configurations, save program output to a file, and add custom VM options. It also covers the setup required to run a Java application, such as creating a new project and configuring the JDK.

### Create a new project

  1. Launch IntelliJ IDEA.

If the Welcome screen opens, click New Project. Otherwise, go to File | New | Project in the main menu.

  2. From the list on the left, select Java. Give the project a name.

  3. Select Maven as the Build system and check the Add sample code.

  4. From the JDK list, select the latest available Oracle OpenJDK version.

If the JDK is installed on your computer, but not defined in the IDE, select Add JDK and specify the path to the JDK home directory.

If you don't have the necessary JDK on your computer, select Download JDK.

  5. Click Create.


![Creating a new project](https://resources.jetbrains.com/help/img/idea/2025.3/run-java-app-project.png)

### Run the application

  1. When the project is created, in the Project tool window (`Alt+1`), locate the src | main | java | Main.java file and open it in the editor.

  2. Replace the existing code with the following code sample:

package org.example; import java.util.stream.Stream; public class Main { public static void main(String[] args) { Stream.iterate(1, i -> i + 1) .limit(10) .forEach(System.out::println); } } 

  3. In the editor, click the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.gutter.run.svg) gutter icon to run the application and select Run 'Main.main()'. 

![Run the application](https://resources.jetbrains.com/help/img/idea/2025.3/run-java-app-gutter-run.png)



IntelliJ IDEA runs your code and shows its output in the Run tool window at the bottom of the screen. The application has run successfully, that is why you will see the `Process finished with exit code 0` message in the output.

![Application has compiled](https://resources.jetbrains.com/help/img/idea/2025.3/run-java-app-successful.png)

When you clicked Run, IntelliJ IDEA created a temporary [run configuration](run-debug-configuration.html) named after the `Main` class. It defines the entry point and the parameters for running the application. So far, we haven't used any startup parameters, but we'll add them later.

The number of temporary configurations is limited to 5 by default, so the older ones are automatically deleted when new ones are added. That is why it is makes sense to save the temporary configurations that you want to keep.

You change the maximum number of temporary configurations in Settings | Advanced Settings | Run/Debug | Temporary configurations limit.

### Save the run configuration

  1. In the main menu, go to Run | Edit Configurations.

  2. In the area on the left, select the Main configuration and click the ![Save Configuration](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.save.svg) icon on the toolbar above. Do not close the dialog yet.

The icons of temporary configurations are transparent. After saving, Main's icon becomes solid.


![Save the run configuration](https://resources.jetbrains.com/help/img/idea/2025.3/run-java-app-save.png)

Enable the Store as project file option to place the run configuration under [version control](version-control-integration.html) and share it with other project contributors.

### Save console output to a file

Now let's copy this configuration and modify it so that the IDE saves the console output to a file every time you run the configuration. This might be useful if you use console output for logging.

  1. In the area on the left, select the Main configuration and click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.copy.svg) on the toolbar. This will create a copy of the run configuration.

  2. In the area on the right, rename the configuration to `SaveConsoleOutput`.

  3. Click Modify options and from the Logs settings group, select Save console output to file. The new Save console output to file field appears in the dialog.

  4. Specify the path to the file to which the IDE will write the output. If the file does not exist, it will be created automatically.

In our case, we will create a file in the project directory, so depending on your operating system and username, the path will look like this: `/Users/me.user/IdeaProjects/RunApplication/console.txt`.

![Save console output to a file](https://resources.jetbrains.com/help/img/idea/2025.3/run-java-app-console-output.png)
  5. Apply the changes and close the dialog.




### Run the saved configuration

  1. Select `SaveConsoleOutput` in the [Run widget](guided-tour-around-the-user-interface.html#toolbar) in the window header and click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.run.run.svg) next to it or press `Shift+F10`. 

![Running a configuration](https://resources.jetbrains.com/help/img/idea/2025.3/run-java-app_widget.png)
  2. When the IDE finishes running the configuration, locate the new file with the console output in the Project tool window and make sure the application's output is there.


![Console output saved to a file](https://resources.jetbrains.com/help/img/idea/2025.3/run-java-app-output-saved.png)

If you store logs in the project directory, add the logs folder to [.gitignore](set-up-a-git-repository.html#ignore-files) to avoid sharing it through VCS. You can also mark the folder as [excluded](content-roots.html#exclude-files-folders) to exclude it from indexing and search.

Run configurations allow you to run the same application with different parameters. Now that you have two configurations, you can choose between them according to your needs. For example, if you do not need to save the console output every single time you run the application, you can run the `Main` configuration that does not have this setting.

Press `Alt+Shift+F10` or use the Run widget in the window header to switch between configurations:

![Run widget switcher](https://resources.jetbrains.com/help/img/idea/2025.3/run-java-app-run-switcher.png)

Let's take a look at another scenario.

### Change the code

Imagine that our code sample has a problem.

  1. In the Main.java file, remove:

Stream.iterate(1, i -> i + 1) .limit(10) .forEach(System.out::println); 

Instead, paste the following code:

var list = Stream.iterate(1, i -> i + 1) .toList(); System.out.println(list.size()); 

  2. In the editor, click the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.gutter.run.svg) gutter icon to run the application and select Run 'Main.main()'.




The application runs for several seconds and then fails with `OutOfMemoryError`. Our program creates an infinite stream of integers and then tries to collect it into a list using the `toList()` method. Since the stream is infinite, the `toList()` method will never return, and the program will keep consuming memory until it fails.

![Application failed with OutOfMemoryError](https://resources.jetbrains.com/help/img/idea/2025.3/run-java-app-failed.png)

If an application fails with `OutOfMemoryError`, we can add a VM option that will dump the memory to a .hprof file before crashing. Later on, we will be able to analyze this file in detail using the built-in [profiler](profiler-intro.html).

### Add the VM options

  1. In the main menu, go to Run | Edit Configurations.

  2. In the area on the left, click the Main configuration and then click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.copy.svg) on the toolbar to clone the configuration. Rename the new configuration to `OutOfMemory`.

  3. Open the Modify options list and click Add VM options.

  4. The VM Options field appears in the dialog. In this field, add the following options with a space between them:

`-Xmx512m -XX:+HeapDumpOnOutOfMemoryError`

![Application failed with OutOfMemoryError](https://resources.jetbrains.com/help/img/idea/2025.3/run-java-app-memory-configuration.png)

`-XX:+HeapDumpOnOutOfMemoryError` specifies that a heap dump should be created in case the app crashes because of `OutOfMemoryError`, and `-Xmx512m` sets the size of the heap to 512 MB so that the heap dump will not be too large.

  5. Apply the changes and close the dialog. 

  6. Select OutOfMemory in the [Run widget](guided-tour-around-the-user-interface.html#toolbar) and click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.run.run.svg) next to it or press `Shift+F10`.




The Run tool window opens showing you that the `OutOfMemoryError` exception has been thrown. Since we have configured the corresponding VM option, the IDE has created an .hprof file in your project directory.

![.hprof file has been created](https://resources.jetbrains.com/help/img/idea/2025.3/run-java-app-hprof.png)

Double-click the created .hprof file to analyze it with the [profiler](profiler-intro.html).

11 November 2024

[List of run/debug configuration templates](list-of-run-debug-configurations.html)[Run compound tasks](run-debug-multiple.html)
