[//]: # (Source: https://www.jetbrains.com/help/idea/run-debug-configuration-maven.html)
[//]: # (Downloaded: 2025-12-17 19:58:24)

## Modify run options

Click Modify options to add more run options or remove some of the default ones described above.

![Add Run Options](https://resources.jetbrains.com/help/img/idea/2025.3/add_run_options.png)

### Operating System

Item| Description  
---|---  
Allow multiple instances| Select this option to allow running multiple instances of this run configuration in parallel. By default, it is disabled, and when you start this configuration while another instance is still running, IntelliJ IDEA suggests stopping the running instance and starting another one. This is helpful when a run configuration consumes a lot of resources and there is no good reason to run multiple instances.  
  
### Java Options

Item| Description  
---|---  
VM options| Specify the options to be passed to the Java virtual machine when launching the application, for example, `-mx`, `-verbose`, and so on.When specifying JVM options, follow these rules:

  * Use spaces to separate individual options.
  * If the value of an option includes spaces, enclose either the value or the actual spaces with double quotes.
  * If an option includes double quotes as part of the value, escape the double quotes using backslashes.
  * You can pass environment variable values to custom Java properties.

-Xmx1024m -Dspaces="some arg" -Dmy.prop=\"quoted_value\" -Dfoo=${MY_ENV_VAR} Use code completion in this field: start typing the name of a flag, and the IDE suggests a list of available command line options. This works for `-XX:` and `-X` options and some standard options that are not configured by IntelliJ IDEA automatically, like `-ea`, but not for `-cp` or `–release`.The `-classpath` option specified in this field overrides the classpath of the module.  
JRE| Specify a version of Java to use in your run configuration.  
  
### Maven Options

Item| Description  
---|---  
Profiles| Specify the profiles to be used separated with space. For more information, refer to [Maven profiles](work-with-maven-profiles.html).  
User settings| Specify the file that contains user-specific configuration for Maven in the text field. If you need to specify another file, check the Override option, click the ellipsis button and select the desired file in the Select Maven Settings File dialog.  
Local repository| By default, the field shows the path to the local directory under the user home that stores the downloads and contains the temporary build artifacts that you have not yet released. If you need to specify another directory, check the Override option, click the ellipsis button and select the desired path in the Select Maven Local Repository dialog.  
Thread Count| Use this field to set the `-T` option for parallel builds. This option is available for Maven 3 and later versions.For more information, refer to [parallel builds in Maven 3](https://cwiki.apache.org/confluence/display/MAVEN/Parallel+builds+in+Maven+3) feature.  
Skip Tests| If this option is checked, the tests will be skipped when running or debugging the Maven project.  
Use plugin registry| Check this option to enable referring to the Maven Plugin Registry. This option corresponds to the `--no-plugin-registry` command-line option.  
Print exception stacktraces| If this option is checked, exception stack traces are generated.This option corresponds to the `--errors` command-line option.  
Always update snapshots| Select this checkbox to always update snapshot dependencies.  
Resolve Workspace artifacts| We recommend that you use this checkbox if you have dependent modules in your project.By default, this checkbox is not selected. In this case, classes of dependent modules are searched in .jar files in a Maven local repository. If you select this checkbox, the classes of the dependent modules will be searched in the module compilation output. In this case, each time you make changes to the dependent module, you don't need to deploy them into a local repository.  
Executed goals recursively| If this option is cleared, the build does not recur into the nested projects. Clearing this option equals to `--non-recursive` command-line option.  
Work offline| f this option is checked, Maven works in the offline mode and uses only those resources that are available locally. This option corresponds to the `--offline` command-line option.  
Checksum policy| Select the desired level of checksum matching while downloading artifacts. You can opt to fail downloading when checksums do not match `--strict-checksums`, or issue a warning `--lax-checksums`.  
Output level| Select the desired level of the output log, which allows plugins to create messages at levels of _debug_ , _info_ , _warn_ , and _error_ , or disable output log.  
Multiproject build fail policy| Specify how to treat a failure in a multiproject build. You can choose to:

  * Fail the build at the very first failure, which corresponds to the command line option `--fail-fast`.
  * Fail the build at the end, which corresponds to the command line option `--fail-at-end`.
  * Ignore failures, which corresponds to the command line option `--fail-never`.

  
  
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
