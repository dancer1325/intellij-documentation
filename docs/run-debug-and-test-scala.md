[//]: # (Source: https://www.jetbrains.com/help/idea/run-debug-and-test-scala.html)
[//]: # (Downloaded: 2025-12-17 19:57:55)

## Run Scala applications

You can run your Scala code through IntelliJ IDEA, use sbt shell, or use [Scala worksheet](work-with-scala-worksheet-and-ammonite.html) for a quick code evaluation.

For a general overview of running programs in IntelliJ IDEA, refer to [Running Applications](running-applications.html).

### Run a Scala application via Intellij IDEA

  1. Create or import a Scala project as you would normally [create or import](creating-and-managing-projects.html) any other project in IntelliJ IDEA.

  2. Open your application in the editor.

  3. Press `Shift+F10` to execute the application. Alternatively, in the editor gutter, click the ![Run](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.run.run.svg) icon and select Run 'name'. 

![Run main](https://resources.jetbrains.com/help/img/idea/2025.3/scala_run_app_editor.png)



### Run a Scala application using the sbt shell

You can run your application using the sbt shell that is a part of any [sbt project](sbt-support.html).

  1. Open your sbt project.

  2. If you want to delegate your builds and imports to sbt, in the sbt tool window, click the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) icon and select sbt Settings.

On the sbt settings page, under the sbt shell select the build option (required sbt 0.13.5+) and click OK to save the changes.

![sbt settings](https://resources.jetbrains.com/help/img/idea/2025.3/sbt_settings_for_running_sbt_shell.png)

This option is also available when you create or import an sbt project.

If you don't want to delegate your builds and imports to sbt, you can still work in the sbt shell (click sbt shell on the status bar) and [run sbt commands](http://www.scala-sbt.org/1.x/docs/Running.html) directly from it including running your application.

  3. In the sbt projects tool window, click the sbt Tasks node.

  4. In the list that opens, select the run task that will run a main method. 

![sbt tool window: run task](https://resources.jetbrains.com/help/img/idea/2025.3/sbt_tool_window_run_task.png)

The result of execution is displayed in sbt shell tool window. 

![sbt shell output](https://resources.jetbrains.com/help/img/idea/2025.3/sbt_shell_run_app.png)



### Reload changes and hot swapping

Sometimes, you need to insert minor changes into your code without shutting down the process. Since the Java VM has a HotSwap feature, IntelliJ IDEA handles these cases automatically when you call Make.

### Alternative ways to run Scala code

For quick code evaluation, you can use a Scala worksheet that enables you to interactively run your code. Press `Ctrl+Alt+Shift+X` to create a light version of the Scala worksheet and `Ctrl+Alt+W` to run it.

Alternatively, you can open Scala REPL and use it to import any class or module of your project and run its methods. For more information, refer to [Scala worksheet, Scala REPL and Ammonite](work-with-scala-worksheet-and-ammonite.html).

If you need, you can also deploy your Scala application to a server. For more information, refer to [Working with Application Servers](application-servers-support.html).
