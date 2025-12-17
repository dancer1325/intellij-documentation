[//]: # (Source: https://www.jetbrains.com/help/idea/big-data-tools-spark-submit.html)
[//]: # (Downloaded: 2025-12-17 19:19:17)

# Spark Submit run configuration

With the [Spark](https://plugins.jetbrains.com/plugin/21700-spark) plugin, you can execute applications on [Spark clusters](https://spark.apache.org/docs/latest/cluster-overview.html). IntelliJ IDEA provides run/debug configurations to run the [spark-submit](https://spark.apache.org/docs/latest/submitting-applications.html) script in Spark’s bin directory. You can execute an application locally or using an SSH configuration.

If you have an Amazon EMR cluster, you can also configure an [EMR connection](big-data-tools-aws-emr.html) and use Amazon EMR steps to submit your application to Spark installed on the EMR cluster. For more information, refer to [Manage Steps](big-data-tools-aws-emr.html#steps).

For Java and Scala applications, you can launch the Spark run configuration in debug mode, under which IntelliJ IDEA connects to a remote Spark driver to debug it. Debugging Spark executors is not available.

### Install the Spark plugin

This functionality relies on the [Spark](https://plugins.jetbrains.com/plugin/21700-spark) plugin, which you need to install and enable. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Marketplace tab, find the Spark plugin, and click Install (restart the IDE if prompted).




### Run an application with the Spark Submit configurations

To quickly create a Spark Submit run configuration, [use the special gutter icon](big-data-tools-spark-tutorial.html#submit-spark-to-emr) in your source Java or Scala code.

  1. Go to Run | Edit Configurations. Alternatively, press `Alt+Shift+F10`, then `0`. 

  2. Click the Add New Configuration button (![Add a run/debug configuration](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)) and select Spark Submit | Cluster.

The Spark Submit | Local and Spark Submit | SSH configurations are deprecated in IntelliJ IDEA 2023.3.

  3. Enter the run configuration name.

  4. In the Remote target list, do one of the following:

     * If you have connected to an [AWS EMR cluster](big-data-tools-aws-emr.html), you can upload your application on it.

     * If you have SSH configurations, you can use them to submit applications to a custom remote server.

     * Otherwise, click Add EMR Connection or Add SSH Connection.

  5. In the Application field, select a way to obtain the application file:

     * Click ![Gradle](https://resources.jetbrains.com/help/img/idea/2025.3/gradle.icons.expui.gradle.svg) to select a Gradle task and artifact.

     * Click ![IDEA artifact](https://resources.jetbrains.com/help/img/idea/2025.3/app.nodes.artifact.svg) to select [an IDEA artifact](compiling-applications.html#package_into_jar).

     * Or click ![Upload local file](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.nodes.folder.svg) to upload a JAR or ZIP file from you local machine.

  6. In the Class field, type the name of the main class of the application.

![Spark Run Configuration](https://resources.jetbrains.com/help/img/idea/2025.3/spark_run_configuration.png)

To check the resulting `spark-submit` command, scroll down to the Result Submit Command section.

  7. You can also specify optional parameters:

     * Run arguments: arguments to run the application.

     * Under Spark Configuration, set up:

       * Cluster manager: select the management method to run an application on a cluster. SparkContext can connect to several types of cluster managers (either Spark’s own standalone cluster manager, Mesos, or YARN). See more details in the [Cluster Mode Overview](https://spark.apache.org/docs/latest/cluster-overview.html#cluster-mode-overview).

       * Deploy mode: cluster or client.

       * Target upload directory: the directory on the remote host to upload the executable files.

       * Spark home: a path to the Spark installation directory.

       * Configs: arbitrary Spark configuration property in key=value format.

       * Properties file: the path to a file with Spark properties.

       * Spark Debug (available for Java and Scala applications):

         * Start Spark driver with debug agent: Start the JDWP agent when you launch this run/debug configuration. This will allow you to connect to a debugger after running the application. Disabling the option disables the debug mode of this configuration.

         * Listening port: specify a debugger port on the server. Leave empty to dynamically assign an available port at runtime.

         * Suspend driver: Suspend the Spark driver process until the debugger is attached (`suspend=y` JDWP agent option). Applied only in debug mode. In run mode, `suspend=n` is always used.

     * Under Dependencies, select files and archives (jars) that are required for the application to be executed.

     * Under Maven, select Maven-specific dependencies. You can add repositories or exclude some packages from the execution context.

     * Under Driver, select Spark Driver settings, such as amount of memory to use for the driver process. For the cluster mode, it is also possible to specify the number of cores.

     * Under Executor, select executor settings, such as the amount of memory and the number of cores.

     * Kerberos: settings for establishing a secured connection with Kerberos.

     * Shell options: select if you want to execute any scripts before the Spark submit.

Enter the path to bash and specify the script to be executed. It is recommended to provide an absolute path to the script.

Select the Interactive checkbox if you want to launch the script in the interactive mode. You can also specify environment variables, for example, `USER=jetbrains`.

     * Advanced Submit Options:

       * Proxy user: a username that is enabled for using proxy for the Spark connection.

       * Driver Java options, Driver library path, and Driver class path: add additional driver options. For more information, refer to [Runtime Environment](https://spark.apache.org/docs/latest/configuration.html#runtime-environment).

       * Archives: comma-separated list of archives to be extracted into the working directory of each executor.

       * Print additional debug output: run spark-submit with the `--verbose` option to print debugging information.

  8. Click OK to save the configuration. Then select configuration from the list of the created configurations and click ![Run](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.run.run.svg).

![Select a configuration](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_select_configuration.png)
  9. Inspect the execution results in the Run tool window.




See also [Create and run Spark application on cluster](big-data-tools-spark-tutorial.html) for an example on how to use this run configuration and monitor the execution results.

11 February 2025

[Spark monitoring](big-data-tools-spark-monitoring.html)[Custom Spark cluster](custom-spark-cluster.html)
