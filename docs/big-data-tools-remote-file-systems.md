[//]: # (Source: https://www.jetbrains.com/help/idea/big-data-tools-remote-file-systems.html)
[//]: # (Downloaded: 2025-12-17 19:19:12)

# Remote File Systems

With the Remote File Systems plugin you can connect to remote storages and manage data on them right from your IDE.

### Install the Remote File Systems plugin

This functionality relies on the [Remote File Systems](https://plugins.jetbrains.com/plugin/21706-remote-file-systems) plugin, which you need to install and enable. 

The Remote File Systems plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Marketplace tab, find the Remote File Systems plugin, and click Install (restart the IDE if prompted).




The plugin provides support for the following remote file systems:

  * [AWS S3](big-data-tools-aws-s3.html)

  * [Google Cloud Storage](big-data-tools-google-cloud-storage.html)

  * [Azure](big-data-tools-azure.html)

  * [Alibaba OSS](big-data-tools-alibaba-oss.html)

  * [Tencent COS](big-data-tools-tencent-cos.html)

  * [MinIO](big-data-tools-minio.html)

  * [DigitalOcean Spaces](big-data-tools-digitalocean-spaces.html)

  * [Linode](big-data-tools-linode.html)

  * [HDFS](big-data-tools-hdfs.html)

  * [Yandex Object Storage](big-data-tools-yandex-object-storage.html)

  * [SFTP](big-data-tools-sftp.html)




Once the plugin is installed, the Big Data Tools window appears in the rightmost group of the [tool windows](guided-tour-around-the-user-interface.html). You can also access it using View | Tool Windows | Big Data Tools.

![Big Data Tools tool window](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_remote_file_systems_tool_window.png)

For the basic operations with the remote file systems, use the tool window toolbar:

Item| Description  
---|---  
![Add connection](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| Add a new connection to a server  
![Delete connection](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| Delete the selected connection  
![Refresh Connection](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.refresh.svg)| Refresh the selected connection  
![Connection settings](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.settings.svg)| Open the connection settings  
![Search in notebooks](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.search.svg)| [Navigate to a file in a storage](big-data-tools-data-files.html#navigate)  
![Open in Editor](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.export.svg)| Open the selected storage, bucket, or folder in a separate tab of your editor  
  
08 October 2024

[Kafka](big-data-tools-kafka.html)[Alibaba OSS](big-data-tools-alibaba-oss.html)
