[//]: # (Source: https://www.jetbrains.com/help/idea/go-plugin-run-debug-configurations.html)
[//]: # (Downloaded: 2025-12-17 19:28:14)

## List of fields in run/debug configurations

The fields that appear in the right-hand pane display the default settings for the selected configuration type.

Name| Description  
---|---  
Run kind| A building scope for your application. File and Package scopes work similarly in tests and compilation/running configurations (in terms of the scope they cover).

  * Directory: build an application in the specified directory as a package, without processing any subdirectories.For test configurations, IntelliJ IDEA runs all the tests in the specified directory and all its subdirectories.
  * File: build an application from files specified in the Files field. To pass multiple file paths, use the vertical bar (`|`) as a delimiter. This configuration is automatically selected when you run your program from scratch files.
  * Package: build a single package with all its dependencies. Specify a full import path to the package that you want to build in the Package path field (for example, `github.com/gorilla/mux`). This configuration is automatically selected when you run the `main` function or a separate test by using the Run icon (![the Run button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.execute.svg)) in the gutter.

  
Package path| A full import path of the package that you want to compile (for example, `github.com/gorilla/mux`). This field is available only when you select the Package run kind.You can press `Ctrl+Space` to see a list of available packages.  
Output directory| A directory for the executable file.  
Run after build| Execute the application after the build.  
Emulate terminal in output console| Executes the application and displays the output in the Run tool window as it would appear in the terminal.  
Working directory| Directory that is used for the built application. If you have any code that creates relative files or directories, they will be relative to this directory.  
Environment| Environment variables for your application.To edit environment variables, click the Browse button at the end of the field. In the Environment Variables dialog, click the Add button and add the environment variables that you need.![Add an environment variable](https://resources.jetbrains.com/help/img/idea/2025.3/go_add_environment_variable.png)  
Go tool arguments| Arguments for the go tool (for example, `-o`). Also, you can use [macros](built-in-macros.html) in this field.  
Use all custom build tags| All tags that are applied during the build. Tags are listed in settings `Ctrl+Alt+S` under Languages & Frameworks | Go Build Tags. For more information, refer to [Build constraints and vendoring](configuring-build-constraints-and-vendoring.html).  
Program arguments| Arguments for the built application. Also, you can use [macros](built-in-macros.html) in this field.  
Run with sudo| Grant sudo privileges for the application.  
Module| Name of the current module.  
Before launch| Add tasks that you want to launch before the launch of the selected run/debug configuration. To add a task click the Add button `Alt+Insert` and select the tool that you want to add.  
Store as project file| Enable this option to save your configuration as a project file and share it with team members through [VCS](version-control-integration.html).
