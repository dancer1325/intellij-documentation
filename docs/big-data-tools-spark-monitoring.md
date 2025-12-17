[//]: # (Source: https://www.jetbrains.com/help/idea/big-data-tools-spark-monitoring.html)
[//]: # (Downloaded: 2025-12-17 19:19:16)

# Spark monitoring

With the [Spark](https://plugins.jetbrains.com/plugin/21700-spark) plugin, you can monitor your [Spark](https://spark.apache.org/) cluster and submitted jobs right in the IDE.

In this chapter:

  1. [Establish a connection to a Spark server from scratch](#connect_to_spark)

In addition to creating a connection manually, you can also quickly [create a connection from an AWS EMR cluster](big-data-tools-aws-emr.html#applications) if you have Spark running on it.

  2. [Establish a connection to a Spark from a Zeppelin notebook](#connection-notebook)

  3. [View job graphs](#dag)

  4. [Filter out the monitoring data](#filter)




### Connect to a Spark server

  1. In the Big Data Tools window, click ![Add a connection](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) and select Spark.

  2. In the Big Data Tools dialog that opens, specify the connection parameters:

![Configure Spark connection](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_spark_connection.png)
     * Name: the name of the connection to distinguish it between the other connections.

     * URL: the URL of the Spark History server (it is usually running on port 18080).

Optionally, you can set up:

     * Per project: select to enable these connection settings only for the current project. Clear the checkbox if you want this connection to be visible in other projects.

     * Enable connection: clear the checkbox if you want to disable this connection. By default, the newly created connections are enabled.

     * Enable tunneling: creates an SSH tunnel to the remote host. It can be useful if the target server is in a private network but an SSH connection to the host in the network is available.

Select the checkbox and specify a configuration of an SSH connection (click ... to create a new SSH configuration).

     * Enable HTTP basic authentication: connection with the HTTP authentication using the specified username and password.

     * Proxy: select if you want to use [IDE proxy settings](settings-http-proxy.html) or if you want to specify custom proxy settings.

  3. Once you fill in the settings, click Test connection to ensure that all configuration parameters are correct. Then click OK.




### Establish connection from Zeppelin using running job

If you have the [Zeppelin](https://plugins.jetbrains.com/plugin/21673-zeppelin) plugin, you can quickly connect to a Spark server by opening a Spark job from a Zeppelin notebook.

  1. In a Zeppelin notebook that involves Spark, run a paragraph.

  2. Click the Open job link. In the notification that opens, click More | Create connection link.

![Creating connection to a Spark server](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_spark_create_connection.png)

If you already have a connection to the Spark History server where the job is running, click Select connection and select it from the list.

  3. In the Big Data Tools dialog that opens, verify the connection settings and click Test connection. If the connection has been established successfully, click OK to finalize configuring.




Once you have established a connection to the Spark server, the Spark monitoring tool window appears.

![Spark monitoring: jobs](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_spark_jobs.png)

At any time, you can open the connection settings in one of the following ways:

  * Go to the Tools | Big Data Tools Settings settings page `Ctrl+Alt+S`.

  * Open the Big Data Tools tool window (View | Tool Windows | Big Data Tools), select a Spark connection, and click ![Connection settings](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.settings.svg).

  * Click ![Connection Settings](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moreVertical.svg) in any tab of the Spark monitoring tool window.




When you select an application in the Spark monitoring tool window, you can use the following tabs to monitor data:

  * Info: high-level information on the submitted application, such as App id or Attempt id.

  * Jobs: a summary of the application jobs. Click a job to see more details on it. Use the Visualization tab to [view the job DAG](#dag).

  * Stages: details of each stage.

  * Environment: the values for the environment and configuration variables.

  * Executors: a process launched for an application that runs tasks and keeps data in memory or disk storage across them. Use the Logs tab to view the executor stdout and stderr logs.

  * Storage: persisted RDDs and DataFrames.

  * SQL: details about SQL queries execution (if used by the application).




You can also preview info on Tasks, units of work that sent to one executor.

For more information about types of data, refer to [Spark documentation](https://spark.apache.org/docs/latest/cluster-overview.html).

### Navigate to source code from DAG graphs

A DAG (Directed Acyclic Graph) represents the logical execution plan of a Spark job. Just like in Spark UI, you can visualize the DAG of a Spark job. With IntelliJ IDEA, you can also quickly navigate from a DAG to a corresponding piece of code in your source file.

  1. Open the Spark monitoring tool window: View | Tool Windows | Spark.

  2. Select an application and open the Jobs tab.

  3. In the Visualization column, click Show.

This will open the job visualization in a new editor tab.

  4. In a graph, double-click any operation.




You will be redirected to your source code file, to the corresponding operation.

![Spark DAG](https://resources.jetbrains.com/help/img/idea/2025.3/spark_dag.png)

### Filter out the monitoring data

  * In the Spark monitoring tool window, use the following filters to filter applications:

    * Filter: type an application name or id.

    * Limit: change the limit of displayed applications or select All to show all of them.

    * Started: filter applications by the start time or select Any.

    * Finished: filter applications by the completion time or select Any.

    * ![Filter](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.filter.svg): show only running or completed applications.

![Job stages](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_spark_filters.png)
  * In the Jobs, Stages, and SQL tabs, you can also use ![Filter](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.filter.svg) to filter data by status.




At any time, you can click ![Refresh](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.refresh.svg) in the Spark monitoring tool window to manually refresh the monitoring data. Alternatively, you can configure the automatic update within a certain time interval using the list located next to the Refresh button.

09 May 2025

[Create and run Spark application on cluster](big-data-tools-spark-tutorial.html)[Spark Submit run configuration](big-data-tools-spark-submit.html)
