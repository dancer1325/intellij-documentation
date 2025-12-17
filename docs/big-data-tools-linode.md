[//]: # (Source: https://www.jetbrains.com/help/idea/big-data-tools-linode.html)
[//]: # (Downloaded: 2025-12-17 19:19:08)

# Linode

### Install the Remote File Systems plugin

This functionality relies on the [Remote File Systems](https://plugins.jetbrains.com/plugin/21706-remote-file-systems) plugin, which you need to install and enable. 

The Remote File Systems plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Marketplace tab, find the Remote File Systems plugin, and click Install (restart the IDE if prompted).




### Connect to Linode

  1. In the Big Data Tools window, click ![Add a connection](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) and select Linode.

  2. In the Big Data Tools dialog that opens, specify the connection parameters:

![Configure Linode connection](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_linode.png)
     * Name: the name of the connection to distinguish it between the other connections.

     * Region: select a region to get buckets from.

     * Choose the way to get buckets:

       * To get specific buckets only, select Custom roots and, in the Roots field, specify the name of the bucket or the path to a directory in the bucket. You can specify multiple names or paths by separating them with a comma.

       * To get all buckets, select All buckets in the account. You can then use the bucket filter to show only buckets with particular names. 

     * Enter access credentials: Access Key and Secret Key.

Optionally, you can set up:

     * Per project: select to enable these connection settings only for the current project. Clear the checkbox if you want this connection to be visible in other projects.

     * Enable connection: clear the checkbox if you want to disable this connection. By default, the newly created connections are enabled.

     * HTTP Proxy: select if you want to use [IDE proxy settings](settings-http-proxy.html) or specify custom proxy settings.

You can also set up Extended Connection Settings:

     * Operation timeout (s): enter a timeout (in seconds) for operations performed on the remote storage, such as getting file info, listing or deleting objects. The default value is 15 seconds.

     * Trust all SSL certificates: select it if you trust the SSL certificate used for this connection and do not want to verify it. This can be useful if, for development purposes, you have a host with a self-signed certificate – verifying it could result in an error.

  3. Once you fill in the settings, click Test connection to ensure that all configuration parameters are correct. Then click OK.




Once you have established a connection, you can view the storage and [work with data files](big-data-tools-data-files.html) in it.

09 May 2025

[Google Cloud Storage](big-data-tools-google-cloud-storage.html)[MinIO](big-data-tools-minio.html)
