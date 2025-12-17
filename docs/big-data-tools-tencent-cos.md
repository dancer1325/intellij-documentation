[//]: # (Source: https://www.jetbrains.com/help/idea/big-data-tools-tencent-cos.html)
[//]: # (Downloaded: 2025-12-17 19:19:22)

# Tencent COS

### Install the Remote File Systems plugin

This functionality relies on the [Remote File Systems](https://plugins.jetbrains.com/plugin/21706-remote-file-systems) plugin, which you need to install and enable. 

The Remote File Systems plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Marketplace tab, find the Remote File Systems plugin, and click Install (restart the IDE if prompted).




### Connect to Tencent COS

  1. In the Big Data Tools window, click ![Add a connection](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) and select Tencent COS.

  2. In the Big Data Tools dialog that opens, specify the connection parameters:

![Tencent connection](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_tencent_connection.png)
     * Name: the name of the connection to distinguish it between the other connections.

     * Region: select a region to get buckets from.

     * Choose the way to get buckets:

       * To get specific buckets only, select Custom roots and, in the Roots field, specify the name of the bucket or the path to a directory in the bucket. You can specify multiple names or paths by separating them with a comma.

       * To get all buckets, select All buckets in the account. You can then use the bucket filter to show only buckets with particular names. 

     * Access key: access key of your Tencent Cloud account.

     * Secret key: secret key of your Tencent Cloud account.

Optionally, you can set up:

     * Per project: select to enable these connection settings only for the current project. Clear the checkbox if you want this connection to be visible in other projects.

     * Enable connection: clear the checkbox if you want to disable this connection. By default, the newly created connections are enabled.

     * APPID: specify your Tencent cloud APPID if you want to create buckets using the IDE.

You can also set up Extended Connection Settings:

     * Operation timeout (s): enter a timeout (in seconds) for operations performed on the remote storage, such as getting file info, listing or deleting objects. The default value is 15 seconds.

     * Show icons for version-enabled buckets (affects the bucket list loading time): show a special icon for buckets that have [versioning enabled in your Tencent cloud](https://www.tencentcloud.com/document/product/436/19881).

  3. Once you fill in the settings, click Test connection to ensure that all configuration parameters are correct. Then click OK.




Once you have established a connection, you can view the storage and [work with data files](big-data-tools-data-files.html) in it.

09 May 2025

[MinIO](big-data-tools-minio.html)[Yandex Object Storage](big-data-tools-yandex-object-storage.html)
