[//]: # (Source: https://www.jetbrains.com/help/idea/launching-groovy-interaction-console.html)
[//]: # (Downloaded: 2025-12-17 19:31:17)

# Groovy Interactive Console

You can open an interactive Groovy console in any project including a Java one and use the console as a temporary file to write and evaluate your code.

If dependencies in your project contain a Groovy library then the specified Groovy library is used to launch the Groovy console. If the dependencies do not contain a Groovy library, then the bundled Groovy library will be used.

The Groovy console becomes available if there is a Groovy library dependency in your project. So, ensure that your existing project has one or create a [new Groovy project](getting-started-with-groovy.html#create_groovy_project).

  1. In the main menu, go to Tools | Groovy Console.

  2. If you have more than one module in your project, click the project's name on the console toolbar and select a module from the list to change a classpath for the console. 

![Groovy_Module_Console.png](https://resources.jetbrains.com/help/img/idea/2025.3/Groovy_Module_Console.png)

The Groovy console starts in a separate tab in the editor.

![groovy_editor_console.png](https://resources.jetbrains.com/help/img/idea/2025.3/groovy_editor_console.png)



### Perform different actions inside the Groovy console

  * You can enter code, the coding assistance is available as you type, or paste code from a different file. Press `Ctrl+Enter` or click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.toolwindows.toolWindowRun.svg) to execute code and view the results in the Run tool window. 

![Groovy console and Run tool window](https://resources.jetbrains.com/help/img/idea/2025.3/groovy_console_output.png)
  * You can refer to a class from the Groovy console. Type the name of the class you need, select it and press `Ctrl+B` to jump to its declaration. 

![Go to Declaration](https://resources.jetbrains.com/help/img/idea/2025.3/groovy_console_class_ref.png)
  * If you have an import statement in your code, you can run a partial selection of code omitting the import statement. The Groovy console will include the omitted part during the execution. 

![Include omitted part of code](https://resources.jetbrains.com/help/img/idea/2025.3/groovy_console_include_omitted.png)



28 June 2024

[Run/Debug Configuration: Groovy](run-debug-configuration-groovy.html)[Getting started with Groovy and Java 11 project](getting-started-with-groovy-java-9-project.html)
