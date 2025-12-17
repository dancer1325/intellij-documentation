[//]: # (Source: https://www.jetbrains.com/help/idea/work-with-gradle-tasks.html)
[//]: # (Downloaded: 2025-12-17 20:07:07)

## Run Gradle tasks

You can use several ways to run Gradle tasks such as run them from the Run Anything window, with a [run configuration](run-debug-gradle.html), from a context menu, and even run several tasks with one run configuration.

You can also run Gradle command line options through the [Run Anything](#run_anything_gradle) window.

### Run a Gradle task in the Run Anything window

  1. In the Gradle tool window, on the toolbar, click ![Execute Gradle task](https://resources.jetbrains.com/help/img/idea/2025.3/gradle.icons.gradle.svg). Alternatively, press `Ctrl` twice to open the Run Anything window. 

  2. In the Run Anything window, start typing a name of the task you want to execute. To execute several tasks, enter task names using space to separate each new task. Alternatively, scroll down to the Gradle tasks section and select the task you need. Press `Enter`.

![Enter a task name](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_task_entered.png)

If you have [linked projects](gradle.html#link_gradle_project) and want to run a task for the specified project then in the Run Anything window, in the top-right corner, from the Project list, select the name of the project and in the search field enter the name of your task.

If you have options such as `offline mode` configured for the project, IntelliJ IDEA will automatically include the configuration into the running scope.

  3. IntelliJ IDEA runs the specified task and displays the result in the Run tool window. 

![Run tool window: Gradle task](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_task_run_result.png)

IntelliJ IDEA also saves the task in the Run Anything window under the Recent section as well as under the Run Configurations node in the Gradle tool window. 

![Run Anything: Recent](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_run_anything_recent.png)



### Run a Gradle task via Run Configurations

You can add some additional parameters to your task, configure it as a [run configuration](run-debug-gradle.html), save it and use that run configuration in your project whenever you need.

  1. Open the Gradle tool window.

  2. Right-click the task for which you want to create the Run configuration.

  3. From the context menu select Modify Run Configuration. 

![Create the task run configuration](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_run_config_create.png)
  4. In Create Run Configuration: 'task name', you can use the [default settings](run-debug-gradle.html#run_default) or configure the [additional options](run-debug-gradle.html#add_advanced) and click OK. 

![Run Configuration for a Gradle task](https://resources.jetbrains.com/help/img/idea/2025.3/run_debug_gradle_task.png)

IntelliJ IDEA displays the task under the Run Configurations node. 

![Gradle tool window: Run Configurations](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_run_config_task_display.png)
  5. Double-click the task to run it or right-click the task and from the context menu select Run. 

![Run Configurations: the context menu](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_config_task_run.png)



### Run a Gradle task from the context menu

  1. Open the Gradle tool window.

  2. Right-click a task that you want to run.

  3. From the context menu select Run 'task name'. 

![Gradle tool window: the context menu](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_task_run_from_menu.png)



### Run several Gradle tasks simultaneously

You can create a [run configuration](run-debug-configuration.html) for several tasks.

  1. Select Run | Edit Configurations `Alt+Shift+F10`.

The [Run/Debug Configurations](run-debug-configurations-dialog.html) dialog opens.

  2. In the Run/Debug Configurations dialog, click ![Add icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select Gradle to add a new configuration. 

![Add new Gradle run/debug configuration](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_run_debug_config_add.png)
  3. On the right side of the Run/Debug Configurations dialog, in the Name field, enter the name of your configuration. Also, you can specify where you want to run your configuration. Use the Run on drop-down list to specify the run target option.

Use the Run section to specify settings for the run configuration.

As an example, check the following settings:

     * Tasks and Arguments \- specify tasks and [arguments](https://docs.gradle.org/current/userguide/gradle_command_line.html) you want to execute with this configuration. You can run more than one task. Click ![the Options icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.inlineVariables.svg) inside the field to open the Tasks and Arguments dialog to select the needed options. 

For example, specify `clean` and `build`, and add the argument `--debug`.

     * Gradle project \- click ![Choose one of registered Gradle projects](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.open.svg) and select the registered Gradle project.

     * If you want to add VM options, click the Modify options link and in the dialog that opens, under Java section, select Add VM options. The VM options field is added to the run configuration, and you can specify the needed parameters. For example, specify `-Xmx3g`.

![Gradle Run/Debug configuration](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_run_debug_config_settings.png)

For more information about run configurations, refer to [Run/debug configurations](run-debug-configuration.html). 

  4. Click OK.

The created configuration is added to the Run Configurations node in the Gradle Projects tool window.

  5. Double-click the configuration to run the task or right-click the configuration and select Run. 

![Gradle tool window: run configuration](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_run_configuration.png)


