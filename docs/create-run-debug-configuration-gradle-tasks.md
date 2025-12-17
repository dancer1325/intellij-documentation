[//]: # (Source: https://www.jetbrains.com/help/idea/create-run-debug-configuration-gradle-tasks.html)
[//]: # (Downloaded: 2025-12-17 19:23:04)

## Before launch

In this area, you can specify tasks to be performed before starting the selected run/debug configuration. The tasks are performed in the order they appear in the list. 

Item| Shortcut| Description  
---|---|---  
![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| `Alt+Insert`| Click this icon to add one of the following available tasks:

  * Launch Web Browser: select this option to have a browser started. In the dialog that opens, select the type of the browser and provide the start URL. Also, specify if you want the browser to be launched with the JavaScript debugger.
  * Run External tool: select to run an external application. In the dialog that opens, select one or multiple applications you want to run. If it is not defined in IntelliJ IDEA yet, add its definition. For more information, refer to [External tools](configuring-third-party-tools.html) and [External tools settings](settings-tools-external-tools.html). 
  * Run Another Configuration: select to execute another run/debug configuration and wait until it finishes before starting the current configuration. If you want to run several configurations in parallel, use a [compound run/debug configuration](run-debug-multiple.html#compound-configs). 
  * Build: select to compile the specified module. The [Build Module command](compiling-applications.html#compile_module) will be executed.If an error occurs during compilation, IntelliJ IDEA won't attempt to start the run/debug configuration.
  * Build Project: select to compile the entire project. The [Build Project command](compiling-applications.html#compile_module) will be executed.If an error occurs during compilation, IntelliJ IDEA won't attempt to start the run/debug configuration.
  * Build, no error check: the same as the Build option, but IntelliJ IDEA will try to start the run/debug configuration irrespective of the compilation results.
  * Build Artifacts: select this option to build an [artifact](working-with-artifacts.html) or artifacts. In the dialog that opens, select the artifact or artifacts that should be built.
  * Run Remote External Tool: adds a [remote SSH external tool](settings-tools-remote-ssh-external-tools.html). 
  * Run Grunt task: select this option to run a Grunt task. In the Grunt task dialog that opens, specify the Gruntfile.js where the required task is defined, select the task to execute, and specify the arguments to pass to the Grunt tool. Specify the location of the Node.js runtime, the parameters to pass to it, and the path to the grunt-cli package.
  * Run gulp task: select this option to run a Gulp task. In the Gulp task dialog that opens, specify the Gulpfile.js where the required task is defined, select the task to execute, and specify the arguments to pass to the Gulp tool. Specify the location of the Node.js runtime, the parameters to pass to it, and the path to the gulp package.
  * Run Maven Goal: select this option to [run a Maven goal](work-with-maven-goals.html). In the dialog that opens, select the goal to be run.
  * Run npm script: select this option to execute an npm script.In the NPM Script dialog that opens, specify the [npm run/debug configuration settings](installing-and-removing-external-software-using-node-package-manager.html#createGruntRunConfig). 
  * Compile TypeScript: select to run the built-in TypeScript compiler and thus make sure that all the changes you made to your TypeScript code are reflected in the generated JavaScript files. In the TypeScript Compile Settings dialog that opens, select or clear the Check errors checkbox to configure the behaviour of the compiler in case any errors are detected: 
    * If the Check errors checkbox is selected, the compiler will show all the errors and the run configuration will not start.
    * If the Check errors checkbox is cleared, the compiler will show all the detected errors but the run configuration still will be launched.
  * Upload files to Remote Host: select this option to have the application files automatically [uploaded to the server](configuring-synchronization-with-a-remote-host.html) according to the default server access configuration.
  * Disconnect Data Source: select this option if you want to disrupt the connection to a data source before the run/debug configuration is run.

  
![the Remove button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| `Alt+Delete`| Click this icon to remove the selected task from the list.  
![Edit](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg)| `Enter`| Click this icon to edit the selected task. Make the necessary changes in the dialog that opens.  
![Method up](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moveUp.svg)![Method down](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moveDown.svg)| `Alt+Up``Alt+Down`| Click these icons to move the selected task one line up or down in the list. The tasks are performed in the order that they appear in the list.  
Show this page| | Select this checkbox to show the run/debug configuration settings prior to actually starting the run/debug configuration.  
Activate tool window| | By default this checkbox is selected and the [Run](run-tool-window.html) or the [Debug](debug-tool-window.html) tool window opens when you start the run/debug configuration.Otherwise, if the checkbox is cleared, the tool window is hidden. However, when the configuration is running, you can open the corresponding tool window for it yourself by pressing `Alt+4` or `Alt+5`.
