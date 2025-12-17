[//]: # (Source: https://www.jetbrains.com/help/idea/big-data-tools-spark-tutorial.html)
[//]: # (Downloaded: 2025-12-17 19:19:18)

# Create and run Spark application on cluster

This tutorial covers a basic scenario of working with Spark: we'll create a simple application, build it with Gradle, upload it to an AWS EMR cluster, and monitor jobs in Spark and Hadoop YARN.

We'll go through the following steps:

  1. [Create a new Spark project from scratch](#create-spark-project) using the Spark project wizard. The wizard lets you select your build tool (SBT, Maven, or Gradle) and JDK and ensures you have all necessary Spark dependencies.

  2. [Submit the Spark application to AWS EMR](#submit-spark-to-emr). We'll use a special gutter icon, which creates a ready-to-use run configuration.

  3. [Monitor the application in Spark monitoring](#open-application-in-spark-history-server)

  4. [Open a Spark job from Hadoop YARN Resource Manager](#hadoop-yarn)




### Install the Spark plugin

This functionality relies on the [Spark](https://plugins.jetbrains.com/plugin/21700-spark) plugin, which you need to install and enable. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Marketplace tab, find the Spark plugin, and click Install (restart the IDE if prompted).




If you are using Spark with Scala, you also have to install the [Scala](https://plugins.jetbrains.com/plugin/1347-scala) plugin.

### Create Spark project

  1. In the main menu, go to File | New | Project.

  2. In the left pane of the New Project wizard, select Spark.

  3. Specify a name for a project and its location.

  4. In the Language list, select Scala.

The Type list is used to define the type of the sample application to be generated. Since we are creating our own application, you can select any type.

  5. In the JDK list, select JDK 8, 11, or 17.

  6. Under Artifact Coordinates, specify the group ID and version. 

![Spark new project wizard](https://resources.jetbrains.com/help/img/idea/2025.3/spark_new_project_wizard_scala.png)
  7. Click Create.




This will create a new Spark project with a basic structure and the build.gradle with Spark dependencies.

### Create Spark application

  1. In the created project, right-click the src | main | scala folder (or press `Alt+Insert`) and select New | Scala Class.

  2. In the Create New Scala Class window that opens, select Object and enter a name, for example `SparkScalaApp`.

  3. Write some Spark code. If you use the `getOrCreate` method of the `SparkSession` class in the application `main` method, a special icon ![](https://resources.jetbrains.com/help/img/idea/2025.3/bigdatatools-metastore-core.icons.expui.sparkRun.svg) will appear in the gutter, which lets you quickly create the run Spark Submit configuration.

For example:

import org.apache.spark.sql.{DataFrame, SparkSession} import org.apache.spark.sql.functions._ object SparkScalaApp { def main(args: Array[String]): Unit = { // Create a SparkSession val spark = SparkSession.builder() .appName("Simple Spark App") .getOrCreate() // Sample data val data = Seq( (1, "Alice", 25), (2, "Bob", 30), (3, "Charlie", 22) ) // Define the schema for the DataFrame val schema = List("id", "name", "age") // Create a DataFrame from the sample data and schema val df: DataFrame = spark.createDataFrame(data).toDF(schema: _*) // Perform a simple transformation (add 5 to the age column) val transformedDF = df.withColumn("age_plus_5", col("age") + 5) // Stop the SparkSession spark.stop() } } 




### Set up SSH access to AWS EMR cluster

The Spark Submit run configuration requires SSH access to an AWS EMR cluster to run the spark-submit command on it.

  1. [Create a connection to AWS EMR](big-data-tools-aws-emr.html) if you don't already have one.

  2. Open the AWS EMR tool window: View | Tool Windows | AWS EMR.

  3. Select a cluster, open the Info tab and click Open SSH Config.

  4. In the SSH Configurations window that opens, check the authentication parameters and provide the path to a private key file. To verify this configuration, click Test connection.




Besides run configurations, you can use the SSH configuration to connect to the cluster master node by clicking ![Connect to master node](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.fileTypes.shell.svg) and to connect to it over SFTP by clicking ![Connect via SFTP](https://resources.jetbrains.com/help/img/idea/2025.3/bigdatatools-plugin-rfs.icons.sftp.svg).

### Submit Spark job to AWS EMR

With the dedicated Spark Submit run configuration, you can instantly build your Spark application and submit it to an AWS EMR cluster. To get artifact to be uploaded to AWS EMR, you can use Gradle tasks, IntelliJ IDEA artifacts, or select an existing JAR file. In this tutorial, we'll use Gradle.

  1. In the gutter, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/bigdatatools-metastore-core.icons.expui.sparkRun.svg) next to the `getOrCreate` method. 

![Spark Crete Run Configuration](https://resources.jetbrains.com/help/img/idea/2025.3/spark_gutter_create_run_configuration.png)
  2. Select Create Spark Submit Configuration.

  3. Specify the following parameters of the run configuration:

     * In the Remote target list, select an AWS EMR cluster. IntelliJ IDEA suggests clusters that have a Spark History server running on them.

     * In Application, click ![Gradle](https://resources.jetbrains.com/help/img/idea/2025.3/gradle.icons.expui.gradle.svg) and select a Gradle artifact.

When you run this configuration, IntelliJ IDEA will build this artifact and then upload it to AWS EMR. You can see the corresponding Run Gradle task and Upload Files Through SFTP steps in the Before launch section.

     * Click Additional customization, enable the Spark Configuration section and, in the Cluster manager list, make sure Hadoop YARN is selected.

  4. Click Run.


![Spark Run Configuration](https://resources.jetbrains.com/help/img/idea/2025.3/spark_run_configuration.png)

This will open the Run tool window with the Gradle task. Once the artifact is built, the Spark Submit task opens in a new tab of the Run tool window.

For more information about this run configuration, refer to [Spark Submit run configuration](big-data-tools-spark-submit.html).

### Open application in Spark History Server

If your application is successfully uploaded to AWS EMR, it will be available in the Spark History server. You'll see the corresponding notification in the Run tool window. You can open it in a browser or in the dedicated Spark monitoring tool window.

  * In the Run tool window, click Open monitoring in the notification that opens.

If you don't have a Spark connection yet, click Create connection instead. You can then click Create default to create a default Spark connection based on the AWS EMR cluster settings.

  * Alternatively, you can click tracking URL in the run configuration output in the Run tool window.


![Spark Run Tool Window](https://resources.jetbrains.com/help/img/idea/2025.3/spark_run_tool_window.png)

For more information about the Spark monitoring tool window, refer to [Spark monitoring](big-data-tools-spark-monitoring.html).

### Open Spark job from Hadoop YARN Resource Manager

If you submit a Spark application to a YARN cluster, it is run as a YARN application, and you can monitor it in the dedicated Hadoop YARN tool window (provided by the Metastore Core plugin). This is what we did in our tutorial when we selected Hadoop YARN as a cluster manager in the Spark Submit run configuration.

If you have not configured Hadoop YARN connection yet, refer to [Hadoop YARN](big-data-tools-hadoop.html).

  1. Open the Hadoop YARN tool window: View | Tool Windows | Hadoop YARN. If you have multiple Hadoop YARN connections, select the needed one using tabs on top of the tool window.

  2. Open the Applications tab and locate your application using the Id column.

  3. Click the address in the Tracking url column.

  4. If you are not redirected to the Spark monitoring tool window, a notification about a missing connection will appear. Click either Select connection to select an existing Spark connection, or More | Create connection to create a new connection.

![Create Spark connection notification](https://resources.jetbrains.com/help/img/idea/2025.3/spark_create_connection_from_hadoop_yarn.png)



This integration with Spark is configured in the Hadoop YARN connection settings. To check or change it, open the Hadoop YARN connection settings (by clicking ![Connection Settings](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moreVertical.svg) in the Hadoop YARN tool window or ![Connection Settings](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) in the Big Data Tools tool window) and select a Spark connection in the Spark monitoring list.

For more information about the Hadoop YARN tool window, refer to [Hadoop YARN](big-data-tools-hadoop.html).

06 June 2025

[Spark](big-data-tools-spark.html)[Spark monitoring](big-data-tools-spark-monitoring.html)
