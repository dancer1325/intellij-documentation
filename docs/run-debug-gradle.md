[//]: # (Source: https://www.jetbrains.com/help/idea/run-debug-gradle.html)
[//]: # (Downloaded: 2025-12-17 19:59:03)

## Add Run Options

Click Modify options in the Run/Debug Configurations dialog to open the list of run options.

The Add Run Options list lets you add more run options to the Run/Debug Configurations dialog or remove some of the default ones from it. The list is divided into various sections, so you can easily navigate through the available options.

![Gradle configuration settings](https://resources.jetbrains.com/help/img/idea/2025.3/modify_options_gradle.png)

### Operating System

Item| Description  
---|---  
Allow multiple instances| Select this option to allow running multiple instances of this run configuration in parallel. By default, it is disabled, and when you start this configuration while another instance is still running, IntelliJ IDEA suggests stopping the running instance and starting another one. This is helpful when a run configuration consumes a lot of resources and there is no good reason to run multiple instances.  
  
### Java

Item| Description  
---|---  
VM options| Specify the options to be passed to the Java virtual machine when launching the application, for example, `-mx`, `-verbose`, and so on.When specifying JVM options, follow these rules:

  * Use spaces to separate individual options.
  * If the value of an option includes spaces, enclose either the value or the actual spaces with double quotes.
  * If an option includes double quotes as part of the value, escape the double quotes using backslashes.
  * You can pass environment variable values to custom Java properties.

-Xmx1024m -Dspaces="some arg" -Dmy.prop=\"quoted_value\" -Dfoo=${MY_ENV_VAR} Use code completion in this field: start typing the name of a flag, and the IDE suggests a list of available command line options. This works for `-XX:` and `-X` options and some standard options that are not configured by IntelliJ IDEA automatically, like `-ea`, but not for `-cp` or `–release`.The `-classpath` option specified in this field overrides the classpath of the module.  
  
### Logs

The following options are related to logging the execution of this configuration. For more information, refer to [Logs](setting-log-options.html). 

Item| Description  
---|---  
Specify logs to be shown in the console| Specify which log files to display while running the application.Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) to add a new log. In the Edit Log Files Aliases dialog, configure the following:

  * Alias: The name of the tab where the log will be displayed.
  * Log File Location: Specify the path to the log file or an [Ant pattern](https://ant.apache.org/manual/dirtasks.html). If several files of a rolling log match the pattern, IntelliJ IDEA will display the most recent one.
  * Show all files coverable by pattern: Show all logs that match the pattern.

For logs in the table, you can configure the following options:

  * Is Active: Display the specified log file.
  * Skip Content: Do not display old log messages from previous runs.

  
Save console output to file| Save the console output to the specified location. Type the path manually or click the browse button and point to the desired location in the dialog that opens.  
Show console when a message is printed to stdout| Activate the console when the application writes to the standard output stream.  
Show console when a message is printed to stderr| Activate the console when the application writes to the standard error stream.  
  
### Code Coverage

The following options are related to code coverage. For more information, refer to [Code coverage](code-coverage.html). 

Item| Description  
---|---  
Specify classes and packages| In this table, specify classes and packages to be measured. Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select ![the Add Class button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.nodes.class.svg) Add Class or ![the Add Package button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.nodes.package.png) Add Package to specify. You can also remove classes and packages from the list by selecting them in the list and clicking the ![remove the package](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) button.  
Exclude classes and packages| Specify classes and packages that you want to exclude from coverage.Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select ![the Add Class button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.nodes.class.svg) Add Class or ![the Add Package button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.nodes.package.png) Add Package to specify classes and packages.  
  
### Before Launch

In this area, you can specify tasks to be performed before starting the selected run/debug configuration. The tasks are performed in the order they appear in the list. 

Item| Description  
---|---  
Add before launch task| Enable this option to add one of the following available tasks:

  * Launch Web Browser: select this option to have a browser started. In the dialog that opens, select the type of the browser and provide the start URL. Also, specify if you want the browser be launched with JavaScript debugger.
  * Run External tool: run an external application. In the dialog that opens, select one or multiple applications you want to run. If it is not defined in IntelliJ IDEA yet, add its definition. For more information, refer to [External tools](configuring-third-party-tools.html).
  * Run Another Configuration: select to execute another run/debug configuration and wait until it finishes before starting the current configuration. If you want to run several configurations in parallel, use a [compound run/debug configuration](run-debug-multiple.html#compound-configs).
  * Run Remote External Tool: add a [remote SSH external tool](settings-tools-remote-ssh-external-tools.html).
  * Run Gradle task: run a [Gradle task](create-run-debug-configuration-gradle-tasks.html). In the dialog that opens, specify the task and provide additional configuration if necessary.
  * Build: select to compile the specified module. The [Build Module](compiling-applications.html#compile_module) action will be executed.If an error occurs during compilation, IntelliJ IDEA won't attempt to start the run/debug configuration.
  * Build Project: select to compile the entire project. The [Build Project](compiling-applications.html#compile_module) action will be executed.If an error occurs during compilation, IntelliJ IDEA won't attempt to start the run/debug configuration.
  * Build, no error check: the same as the Build option, but IntelliJ IDEA will try to start the run/debug configuration irrespective of the compilation results.
  * Build Artifacts: select this option to build an [artifact](working-with-artifacts.html) or artifacts. In the dialog that opens, select the artifact or artifacts that should be built.
  * Run Maven Goal: select this option to [run a Maven goal](work-with-maven-goals.html). In the dialog that opens, select the goal to be run.
  * Run Grunt task: select this option to run a Grunt task. In the Grunt task dialog that opens, specify the Gruntfile.js where the required task is defined, select the task to execute, and specify the arguments to pass to the Grunt tool. Specify the location of the Node.js runtime, the parameters to pass to it, and the path to the grunt-cli package.
  * Run gulp task: select this option to run a Gulp task. In the Gulp task dialog that opens, specify the Gulpfile.js where the required task is defined, select the task to execute, and specify the arguments to pass to the Gulp tool. Specify the location of the Node.js runtime, the parameters to pass to it, and the path to the gulp package.
  * Run npm script: select this option to execute an npm script.In the NPM Script dialog that opens, specify the [npm run/debug configuration settings](installing-and-removing-external-software-using-node-package-manager.html#createGruntRunConfig).
  * Compile TypeScript: select to run the built-in TypeScript compiler and thus make sure that all the changes you made to your TypeScript code are reflected in the generated JavaScript files. In the TypeScript Compile Settings dialog that opens, select or clear the Check errors checkbox to configure the behaviour of the compiler in case any errors are detected: 
    * If the Check errors checkbox is selected, the compiler will show all the errors and the run configuration will not start.
    * If the Check errors checkbox is cleared, the compiler will show all the detected errors but the run configuration still will be launched.
  * Disconnect Data Source: select this option if you want to disrupt the connection to a data source before the run/debug configuration is run.

  
Open run/debug tool window when started| Depending on the type of configuration, open the [Run](run-tool-window.html), [Debug](debug-tool-window.html), or [Services](services-tool-window.html) tool window when you start this run configuration. If this option is disabled, you can open the tool window manually:

  * View | Tool Windows | Run or `Alt+4`
  * View | Tool Windows | Debug or `Alt+5`
  * View | Tool Windows | Services or `Alt+8`

  
Focus run/debug tool window when started| Focus on the run configuration tool window when the tests are running.  
Show the run/debug configuration settings before start| Show the run configuration settings before actually starting it.  
  
### Gradle

Item| Description  
---|---  
Debug all tasks on the execution graph| When you select this option, every task in the execution graph will be debugged. For example, all the dependent tasks of the task you are trying to debug.  
Debug forked Gradle tasks in separate debug tabs| Select this option to run a debugging process in a separate tab in the Debug tool window.  
Run as test| By default, this option is disabled. In such case, IntelliJ IDEA doesn't open the Run tool window and doesn't rerun tests tasks if they are up to date.However, if IntelliJ IDEA finds test tasks in the run configuration, those are highlighted in the [Gradle](jetgradle-tool-window.html) tool window, IntelliJ IDEA doesn't rerun test tasks, but opens the Gradle tool window.The option becomes enabled when you trigger the test execution from the editor using ![the Run button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.run.run.svg) in the gutter or the context menu.In this case, IntelliJ IDEA opens the Run tool window and reruns the test tasks each time the execution is triggered even if the tests are up to date.This option might be helpful in controlling the rerunning process of the test tasks in your project.
