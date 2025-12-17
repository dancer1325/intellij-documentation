[//]: # (Source: https://www.jetbrains.com/help/idea/custom-spark-cluster.html)
[//]: # (Downloaded: 2025-12-17 19:23:42)

# Custom Spark cluster

In the [Spark Submit run configuration](big-data-tools-spark-submit.html), you can use AWS EMR or Dataproc as remote servers to run your applications. Besides these two options, you can also configure your own custom Spark cluster: Set up an SSH configuration to connect to a remote server and, optionally, configure connections to a Spark History server and an SFTP connection.

### Create a Custom Spark cluster

  1. In the Big Data Tools window, click ![Add a connection](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) and select Custom Spark Cluster.

  2. In the first step of the window that opens, select an SSH configuration and click Next. This SSH configuration will be used to connect to a server on which spark-submit is installed. 

![Select Spark Submit](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_custom_spark_cluster_step_1.png)
  3. If you want to [monitor Spark jobs](big-data-tools-spark-monitoring.html) in the IDE, specify parameters for establishing a connection to a Spark history server in the second step of the wizard. Specify your custom parameters or use default settings, which will create a connection to `localhost:18080` using an SSH tunneling.

Otherwise, select I don't need a connection to Spark History server.

![Select Spark Submit](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_custom_spark_cluster_step_2.png)
  4. If you need an SFTP connection to your Spark cluster, specify its settings in the third step of the wizard.

Otherwise, select I don't need an SFTP connection to Driver Node.

![Select Spark Submit](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_custom_spark_cluster_step_3.png)



If you've set up both Spark History and SFTP connections, they will be available under Custom Spark Cluster in the Big Data Tools tool window.

![Select Spark Submit](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_custom_spark_cluster_result.png)

You can now select this cluster as a remote target in the [Spark Submit run configuration](big-data-tools-spark-submit.html). When you launch this run configuration, you'll be able to open the Spark job in the Services tool window by clicking the link in the application output.

09 May 2025

[Spark Submit run configuration](big-data-tools-spark-submit.html)[Spark DataFrame coding assistance](big-data-tools-spark-coding-assistance.html)
