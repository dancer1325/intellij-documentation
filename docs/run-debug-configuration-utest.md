[//]: # (Source: https://www.jetbrains.com/help/idea/run-debug-configuration-utest.html)
[//]: # (Downloaded: 2025-12-17 19:58:56)

## Configuration tab

Item| Description  
---|---  
Test kind| From list, select the scope for your tests and fill in the fields depending on your selection:

  * Test name: select this option to run the specified Scala test. The name of the test appears in the Test Name field.
  * All in package: run all unit tests in a package. Specify the package in the field to the right.
  * Class: run all unit tests in a class. Specify the fully qualified name of the class in the field to the right.
  * Regular expression: run all unit tests with the class name and/or the test name match the given regular expressions.

  
VM options| Specify the options to be passed to the Java virtual machine when launching the application, for example, `-mx`, `-verbose`, and so on.When specifying JVM options, follow these rules:

  * Use spaces to separate individual options.
  * If the value of an option includes spaces, enclose either the value or the actual spaces with double quotes.
  * If an option includes double quotes as part of the value, escape the double quotes using backslashes.
  * You can pass environment variable values to custom Java properties.

-Xmx1024m -Dspaces="some arg" -Dmy.prop=\"quoted_value\" -Dfoo=${MY_ENV_VAR} Use code completion in this field: start typing the name of a flag, and the IDE suggests a list of available command line options. This works for `-XX:` and `-X` options and some standard options that are not configured by IntelliJ IDEA automatically, like `-ea`, but not for `-cp` or `–release`.The `-classpath` option specified in this field overrides the classpath of the module.  
Environment variables| Click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.inlineVariables.svg) to open the Environment Variables dialog where you can create variables and specify their values.  
Test options| Use this field to specify the additional test options.If there is not enough space, you can click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.expandComponent.svg) and enter the string in the dialog that opens.  
Working directory| Specify the working directory to be used for running the application. This directory is the starting point for all relative input and output paths. By default, the working directory is the project root.  
Use classpath of module| From this list, select the module whose classpath will be used to run the application.  
Print information messages to console| Select this checkbox if you want to print information messages to the Scala console.  
  
### Code Coverage tab

Use this tab to configure [code coverage](code-coverage.html) monitoring options.

Item| Description  
---|---  
Packages and classes to include in coverage data| Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select ![the Add Class button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.nodes.class.svg) Add Class or ![the Add Package button](https://resources.jetbrains.com/help/img/idea/2025.3/app.nodes.package.svg) Add Package to specify classes and packages to be measured. You can also remove classes and packages from the list by selecting them in the list and clicking the ![remove the package](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) button.  
Packages and classes to exclude from coverage data| Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select ![the Add Class button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.nodes.class.svg) Add Class or ![the Add Package button](https://resources.jetbrains.com/help/img/idea/2025.3/app.nodes.package.svg) Add Package to specify classes and packages that should not be measured. You can also remove classes and packages from the list by selecting them in the list and clicking the ![remove the package](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) button.  
  
### Logs tab

Use this tab to specify which log files generated while running or debugging should be displayed in the console, that is, on the dedicated tabs of the [Run](run-tool-window.html) or [Debug tool window](debug-tool-window.html).

Item| Description  
---|---  
Is Active| Select checkboxes in this column to have the log entries displayed in the corresponding tabs in the [Run tool window](run-tool-window.html) or [Debug tool window](debug-tool-window.html).  
Log File Entry| The read-only fields in this column list the log files to show. The list can contain:

  * Full paths to specific files.
  * [Ant patterns](http://ant.apache.org/manual/dirtasks.html#patterns) that define the range of files to be displayed.
  * Aliases to substitute for full paths or patterns. These aliases are also displayed in the headers of the tabs where the corresponding log files are shown.If a log entry pattern defines more than one file, the tab header shows the name of the file instead of the log entry alias.

  
Skip Content| Select this checkbox to have the previous content of the selected log skipped.  
Save console output to file| Select this checkbox to save the console output to the specified location. Type the path manually, or click the browse button and point to the desired location in the dialog that opens.  
Show console when a message is printed to standard output stream| Select this checkbox to activate the output console and bring it forward if an associated process writes to Standard.out.  
Show console when a message is printed to standard error stream| Select this checkbox to activate the output console and bring it forward if an associated process writes to Standard.err.  
![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| Click this button to open the Edit Log Files Aliases dialog where you can select a new log entry and specify an alias for it.  
![the Edit button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg)| Click this button to edit the properties of the selected log file entry in the Edit Log Files Aliases dialog.  
![the Delete button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| Click this button to remove the selected log entry from the list.  
  
### Common settings

When you edit a run configuration (but not a run configuration template), you can specify the following options:

Item| Description  
---|---  
Name| Specify a name for the run configuration to quickly identify it among others when editing or running.  
Allow multiple instances| Allow running multiple instances of this run configuration in parallel.By default, it is disabled, and when you start this configuration while another instance is still running, IntelliJ IDEA suggests stopping the running instance and starting another one. This is helpful when a run configuration consumes a lot of resources and there is no good reason to run multiple instances.  
Store as project file| Save the file with the run configuration settings to share it with other team members. The default location is .idea/runConfigurations. However, if you do not want to share the .idea directory, you can save the configuration to any other directory within the project.By default, it is disabled, and IntelliJ IDEA stores run configuration settings in .idea/workspace.xml.  
  
### Toolbar

The tree view of run/debug configurations has a toolbar that helps you manage configurations available in your project as well as adjust default configurations templates.

Item| Shortcut| Description  
---|---|---  
![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| `Alt+Insert`| Create a run/debug configuration.  
![the Remove button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| `Alt+Delete`| Delete the selected run/debug configuration. Note that you cannot delete default configurations.  
![Copy](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.copy.svg)| `Ctrl+D`| Create a copy of the selected run/debug configuration. Note that you create copies of default configurations.  
![Save configuration](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.save.svg)| | The button is displayed only when you select a [temporary configuration](run-debug-configuration.html). Click this button to save a temporary configuration as permanent.  
![Move into new folder / Create new folder](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.actions.newFolder.svg)| | Move into new folder / Create new folder. You can group run/debug configurations by [placing them into folders](run-debug-configuration.html#config-folders).To create a folder, select the configurations within a category, click ![Folder](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.nodes.folder.svg), and specify the folder name. If only a category is in focus, an empty folder is created.Then, to move a configuration into a folder, between the folders or out of a folder, use drag or ![Move Up](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moveUp.svg) and ![Move Down](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moveDown.svg) buttons.To remove grouping, select a folder and click ![Remove Configuration](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg).  
![Sort configurations](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.objectBrowser.sortAlphabetically.svg)| |  Click this button to sort configurations in the alphabetical order.  
  
### Before launch

In this area, you can specify tasks to be performed before starting the selected run/debug configuration. The tasks are performed in the order they appear in the list. 

Item| Shortcut| Description  
---|---|---  
![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| `Alt+Insert`| Click this icon to add one of the following available tasks:

  * Launch Web Browser: select this option to have a browser started. In the dialog that opens, select the type of the browser and provide the start URL. Also, specify if you want the browser to be launched with the JavaScript debugger.
  * Run External tool: select to run an external application. In the dialog that opens, select one or multiple applications you want to run. If it is not defined in IntelliJ IDEA yet, add its definition. For more information, refer to [External tools](configuring-third-party-tools.html) and [External tools settings](settings-tools-external-tools.html). 
  * Run Another Configuration: select to execute another run/debug configuration and wait until it finishes before starting the current configuration. If you want to run several configurations in parallel, use a [compound run/debug configuration](run-debug-multiple.html#compound-configs). 
  * Build Artifacts: select this option to build an [artifact](working-with-artifacts.html) or artifacts. In the dialog that opens, select the artifact or artifacts that should be built.
  * Run Remote External Tool: adds a [remote SSH external tool](settings-tools-remote-ssh-external-tools.html). 
  * Run Grunt task: select this option to run a Grunt task. In the Grunt task dialog that opens, specify the Gruntfile.js where the required task is defined, select the task to execute, and specify the arguments to pass to the Grunt tool. Specify the location of the Node.js runtime, the parameters to pass to it, and the path to the grunt-cli package.
  * Run gulp task: select this option to run a Gulp task. In the Gulp task dialog that opens, specify the Gulpfile.js where the required task is defined, select the task to execute, and specify the arguments to pass to the Gulp tool. Specify the location of the Node.js runtime, the parameters to pass to it, and the path to the gulp package.
  * Run Maven Goal: select this option to [run a Maven goal](work-with-maven-goals.html). In the dialog that opens, select the goal to be run.
  * Run npm script: select this option to execute an npm script.In the NPM Script dialog that opens, specify the [npm run/debug configuration settings](installing-and-removing-external-software-using-node-package-manager.html#createGruntRunConfig). 
  * Compile TypeScript: select to run the built-in TypeScript compiler and thus make sure that all the changes you made to your TypeScript code are reflected in the generated JavaScript files. In the TypeScript Compile Settings dialog that opens, select or clear the Check errors checkbox to configure the behaviour of the compiler in case any errors are detected: 
    * If the Check errors checkbox is selected, the compiler will show all the errors and the run configuration will not start.
    * If the Check errors checkbox is cleared, the compiler will show all the detected errors but the run configuration still will be launched.
  * Disconnect Data Source: select this option if you want to disrupt the connection to a data source before the run/debug configuration is run.

  
![the Remove button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| `Alt+Delete`| Click this icon to remove the selected task from the list.  
![Edit](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg)| `Enter`| Click this icon to edit the selected task. Make the necessary changes in the dialog that opens.  
![Method up](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moveUp.svg)![Method down](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moveDown.svg)| `Alt+Up``Alt+Down`| Click these icons to move the selected task one line up or down in the list. The tasks are performed in the order that they appear in the list.  
Show this page| | Select this checkbox to show the run/debug configuration settings prior to actually starting the run/debug configuration.  
Activate tool window| | By default this checkbox is selected and the [Run](run-tool-window.html) or the [Debug](debug-tool-window.html) tool window opens when you start the run/debug configuration.Otherwise, if the checkbox is cleared, the tool window is hidden. However, when the configuration is running, you can open the corresponding tool window for it yourself by pressing `Alt+4` or `Alt+5`.
