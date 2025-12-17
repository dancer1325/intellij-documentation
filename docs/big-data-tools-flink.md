[//]: # (Source: https://www.jetbrains.com/help/idea/big-data-tools-flink.html)
[//]: # (Downloaded: 2025-12-17 19:19:00)

# Flink monitoring

With the [Flink](https://plugins.jetbrains.com/plugin/21702-flink) plugin, you can monitor and submit [Apache Flink](https://flink.apache.org/) jobs.

Typical workflow:

  1. [Establish connection to a Flink server](#connect_to_flink)

  2. Monitor Flink jobs using the dedicated tool window that reflects the Apache Flink Dashboard

  3. [Submit new jobs to the Flink cluster](#submit)




### Connect to a Flink server

  1. In the Big Data Tools window, click ![Add a connection](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) and select Flink.

  2. In the Big Data Tools dialog that opens, specify the connection parameters:

![Configure Flink connection](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_flink_connection.png)
     * Name: the name of the connection to distinguish it between the other connections.

     * URL: specify the URL of your Apache Flink Dashboard.

Optionally, you can set up:

     * Per project: select to enable these connection settings only for the current project. Clear the checkbox if you want this connection to be visible in other projects.

     * Enable connection: clear the checkbox if you want to disable this connection. By default, the newly created connections are enabled.

     * Enable tunneling: creates an SSH tunnel to the remote host. It can be useful if the target server is in a private network but an SSH connection to the host in the network is available.

Select the checkbox and specify a configuration of an SSH connection (click ... to create a new SSH configuration).

     * Enable HTTP basic authentication: connection with the HTTP authentication using the specified username and password.

     * Proxy: select if you want to use [IDE proxy settings](settings-http-proxy.html) or if you want to specify custom proxy settings.

  3. Once you fill in the settings, click Test connection to ensure that all configuration parameters are correct. Then click OK.




Once you have established a connection to the Flink server, the Flink tool window appears, which reflects the Apache Flink Dashboard.

Preview jobs, their configuration, exceptions, and checkpoints. Use the Filter field to filter jobs by name or click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.filter.svg) to filter them by status. If you have a running job, you can click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.suspend.svg) to terminate it.

![Kafka connection: topics](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_flink_jobs.png)

View nodes that run your tasks, view and download their logs, stdout, and thread dumps.

![Kafka connection: topics](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_flink_task_managers.png)

View the Job Manager, view and download logs and stdout.

![Kafka connection: topics](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_flink_job_manager.png)

View uploaded JAR files, filter them by name or entry class, and [submit new Flink jobs](#submit).

![Kafka connection: topics](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_flink_submit_new_job.png)

### Submit New Job

  1. In the Flink tool window, open the Submit New Job tab.

  2. If a JAR file of your application is not uploaded yet to the Flink cluster, click ![Add a connection](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select a new file.

  3. Select the uploaded file and click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.execute.svg).

  4. In the Submit JAR file window that opens, configure the following parameters:

     * Allow non-restored state: allow skipping state of the savepoint that cannot be mapped to the new program (equivalent of the [allowNonRestoredState](https://nightlies.apache.org/flink/flink-docs-release-1.15/docs/ops/state/savepoints/#allowing-non-restored-state) option).

     * Entry class: enter the program entry class.

     * Program arguments: enter the program arguments.

     * Parallelism: enter a number of parallel instances of a task. Leave it blank if you need only one task instance.

     * Savepoint path: enter the path of the job’s execution state image ([savepoint](https://nightlies.apache.org/flink/flink-docs-master/docs/ops/state/savepoints/)).

![Submit JAR File dialog](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_flink_submit_new_job_dialog.png)



Once you have submitted the job, you can preview its status, start time, and other parameters in the [Jobs](#jobs) tab.

09 May 2025

[AWS Glue](big-data-tools-aws-glue.html)[Zeppelin notebooks](big-data-tools-zeppelin-notebooks.html)
