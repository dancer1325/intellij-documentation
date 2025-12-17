[//]: # (Source: https://www.jetbrains.com/help/idea/big-data-tools-spark.html)
[//]: # (Downloaded: 2025-12-17 19:19:20)

# Spark

With the [Spark](https://plugins.jetbrains.com/plugin/21700-spark) plugin, you can create, submit, and monitor your [Spark](https://spark.apache.org/) jobs right in the IDE. The plugin features include:

  * The Spark new project wizard, which lets you quickly create a Spark project with needed dependencies.

  * The Spark Submit run configuration to build and upload your Spark application to a cluster. For Scala files, there is also a special icon in the gutter, which lets you create this configuration even faster. 

  * The Spark monitoring tool window to monitor submitted jobs, view DAG visualizations, and more. This includes jobs submitted from the Spark Submit run configurations and EMR steps. If you have the [Zeppelin](https://plugins.jetbrains.com/plugin/21673-zeppelin) plugin installed, you can also open Spark jobs from Zeppelin notebooks.

  * Integration with other big data tools without leaving the IDE (open Spark applications from AWS EMR, navigate to Spark jobs from Hadoop YARN, view logs in S3 storages).




### Install the Spark plugin

This functionality relies on the [Spark](https://plugins.jetbrains.com/plugin/21700-spark) plugin, which you need to install and enable. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Marketplace tab, find the Spark plugin, and click Install (restart the IDE if prompted).




Prior to IntelliJ IDEA 2023.2, Spark was a part of the Big Data Tools plugin. In IntelliJ IDEA 2023.2, the plugin was divided into [six plugins](https://plugins.jetbrains.com/bundles/8-big-data-tools). If you used Big Data Tools in 2023.1 or before, then after updating IntelliJ IDEA to 2023.2, you will have all these new plugins automatically installed, including Spark.

If you install the Spark plugin, the following auxiliary plugins are automatically installed:

  * Metastore Core lets you connect to data processing and monitoring platforms, such as AWS EMR, Google Cloud Dataproc, or Hadoop YARN Resource Manager.

  * Remote File Systems lets you connect to remote storages, such as AWS S3, Google Cloud Storage, Microsoft Azure.

  * Big Data File Viewer provides a preview for Parquet, ORC, and Avro files.

  * Big Data Tools Core facilitates integration with big data tools — for example, it lets you share MFA and OAuth 2.0 data between AWS Glue authentication in Kafka schema registry and other AWS connections (such as AWS S3, AWS EMR, or AWS Glue monitoring).




In this chapter:

  * [Tutorial on how to create a Spark application](big-data-tools-spark-tutorial.html) using the new project wizard and upload it to an AWS EMR cluster.

  * If you want to monitor existing jobs, learn more about the [Spark monitoring tool window](big-data-tools-spark-monitoring.html).

  * If you want to submit a Spark application to a cluster, learn more about [Spark Submit run configuration](big-data-tools-spark-submit.html)




11 February 2024

[Configure Big Data Tools environment](big-data-tools-configuration.html)[Create and run Spark application on cluster](big-data-tools-spark-tutorial.html)
