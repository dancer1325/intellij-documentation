[//]: # (Source: https://www.jetbrains.com/help/idea/big-data-tools-cloudflare-r2.html)
[//]: # (Downloaded: 2025-12-17 19:18:53)

# Cloudflare R2

### Install the Remote File Systems plugin

This functionality relies on the [Remote File Systems](https://plugins.jetbrains.com/plugin/21706-remote-file-systems) plugin, which you need to install and enable. 

The Remote File Systems plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Marketplace tab, find the Remote File Systems plugin, and click Install (restart the IDE if prompted).




### Connect to Cloudflare R2

  1. In the Big Data Tools window, click ![Add a connection](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) and select Cloudflare R2.

  2. In the Big Data Tools dialog that opens, specify the connection parameters:

![Configure Cloudflare R2 connection](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_cloudflare_connection.png)
     * Name: the name of the connection to distinguish it between the other connections.

     * Select Cloudflare R2 and enter your Account ID.

Alternatively, select Custom endpoint and enter the endpoint URL.

     * Choose the way to get buckets:

       * To get specific buckets only, select Custom roots and, in the Roots field, specify the name of the bucket or the path to a directory in the bucket. You can specify multiple names or paths by separating them with a comma.

       * To get all buckets, select All buckets in the account. You can then use the bucket filter to show only buckets with particular names. 

     * In the Access Key and Secret Key boxes, enter your R2 Storage [credentials](https://developers.cloudflare.com/r2/api/s3/tokens/).

     * HTTP Proxy: select if you want to use [IDE proxy settings](settings-http-proxy.html) or specify custom proxy settings.

Optionally, you can select:

     * Per project: select to enable these connection settings only for the current project. Clear the checkbox if you want this connection to be visible in other projects.

     * Enable connection: clear the checkbox if you want to disable this connection. By default, the newly created connections are enabled.

You can also set up Extended Connection Settings:

     * Operation timeout (s): enter a timeout (in seconds) for operations performed on the remote storage, such as getting file info, listing or deleting objects. The default value is 15 seconds.

     * Trust all SSL certificates: select it if you trust the SSL certificate used for this connection and do not want to verify it. This can be useful if, for development purposes, you have a host with a self-signed certificate – verifying it could result in an error.




Once you have established a connection, you can view the storage and [work with data files](big-data-tools-data-files.html) in it.

09 May 2025

[Azure](big-data-tools-azure.html)[DigitalOcean Spaces](big-data-tools-digitalocean-spaces.html)
