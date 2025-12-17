[//]: # (Source: https://www.jetbrains.com/help/idea/big-data-tools-hadoop.html)
[//]: # (Downloaded: 2025-12-17 19:19:02)

# Hadoop YARN

With IntelliJ IDEA, you can monitor your [Hadoop YARN](https://hadoop.apache.org/docs/current/hadoop-yarn/hadoop-yarn-site/YARN.html) metrics.

This functionality relies on the [Metastore Core](https://plugins.jetbrains.com/plugin/21712-metastore-core/reviews) plugin, which is installed automatically if you install the [Spark](big-data-tools-spark.html) or the [Flink](big-data-tools-flink.html) plugin.

Typical workflow:

  1. [Establish connection to a Hadoop server](#connect_to_hadoop)

  2. [Adjust the preview layout](#monitoring)

  3. [Filter out the parameters to monitor](#filter)




### Connect to a Hadoop server

  1. In the Big Data Tools window, click ![Add a connection](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) and select Hadoop YARN.

  2. In the Big Data Tools dialog that opens, specify the connection parameters:

![Configure Hadoop connection](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_hadoop_monitoring_connection.png)
     * Name: the name of the connection to distinguish it between the other connections.

     * URL: the URL of the Hadoop server.

Optionally, you can set up:

     * Per project: select to enable these connection settings only for the current project. Clear the checkbox if you want this connection to be visible in other projects.

     * Enable connection: clear the checkbox if you want to disable this connection. By default, the newly created connections are enabled.

     * Enable tunneling. This option creates an SSH tunnel to the remote host. It can be useful if the target server is in a private network but an SSH connection to the host in the network is available.

Select the checkbox and specify a configuration of an SSH connection (click ... to create a new SSH configuration).

     * Enable HTTP basic authentication: connection with the HTTP authentication using the specified username and password.

     * Proxy: select if you want to use [IDE proxy settings](settings-http-proxy.html) or if you want to specify custom proxy settings.

     * You can also reuse any of the existing Spark connections. Just select it from the Spark Monitoring list.

  3. Once you fill in the settings, click Test connection to ensure that all configuration parameters are correct. Then click OK.




At any time, you can open the connection settings in one of the following ways:

  * Go to the Tools | Big Data Tools settings page `Ctrl+Alt+S`.

  * Click ![settings](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) on the Hadoop YARN tool window toolbar.




Once you have established a connection to the Hadoop server, the Hadoop YARN tool window appears. It consists of the several areas to monitor data for:

The detailed information about the cluster metrics and resources powered by the Resource Manager.

![Hadoop YARN: Cluster info](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_hadoop_monitoring_info.png)

Presents information about the nodes responsible for tasks execution.

![Hadoop YARN: notes](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_hadoop_monitoring_nodes.png)

Provides the detailed information about the selected data node, including node resource allocation.

![Hadoop YARN: Node labels](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_hadoop_monitoring_node_labels.png)

The detailed overview of the users' applications, including application metrics and execution attempts.

![Hadoop YARN: Applications](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_hadoop_monitoring_applications.png)

Monitoring tools, such as connection settings, log information, server stacks details, and server metrics.

![Hadoop YARN: Tools](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_hadoop_monitoring_tools.png)

For more information about types of data, refer to [Hadoop documentation](https://hadoop.apache.org/docs/current/hadoop-yarn/hadoop-yarn-site/YARN.html).

### Adjust layout

  * In the list of the applications, select one to study.

  * To manage visibility of the monitoring areas, use the following buttons:

Item| Description  
---|---  
![Preview attempts](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.listFiles.svg)| Shows the list of execution attempts.  
![Preview details](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.previewDetails.svg)| Shows application details.  
  
![Showing application details](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_hadoop_monitoring_applications_details.png)
  * To focus on a particular application, click the Open in a separate tab link in the Application details monitoring area.

![Click to preview in a separate tab](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_haddop_monitoring_open_in_separate.png)

The application details will be shown in a separate tab.

![View an application in a separate tab](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_hadoop_monitoring_applications_separate.png)
  * Click ![Preview on web](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.web.svg) to preview any monitoring data in a browser.




Once you have set up the layout of the monitoring window, opened or closed some preview areas, you can filter the monitoring data to preview particular parameters.

### Filter out the monitoring data

  * Use the filter button (![Filter application status](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.filter.svg)) in the monitoring tabs to show details for applications with specific status. Select the specific application statuses you want to monitor.

You can also filter the list of applications by a username, start time, and end time. Besides, you can specify the limit of the items in the filtered list.

![Hadoop YARN: Applications](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_hadoop_monitoring_applications.png)
  * Manage content within a table:

    * Click a column header to change the order of data in the column.

    * Click Show/Hide columns on the toolbar to select the columns to be shown in the table:

![Select columns to show in the table](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_hadoop_filter_table.png)



At any time, you can click ![Refresh](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.refresh.svg) on the Hadoop YARN tool window to manually refresh the monitoring data. Alternatively, you can configure the automatic update within a certain time interval in the list located next to the Refresh button. You can select 5, 10, or 30 seconds.

09 May 2025

[Amazon EMR](big-data-tools-aws-emr.html)[Hive Metastore](big-data-tools-hive.html)
