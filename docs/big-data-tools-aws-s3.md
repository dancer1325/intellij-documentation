[//]: # (Source: https://www.jetbrains.com/help/idea/big-data-tools-aws-s3.html)
[//]: # (Downloaded: 2025-12-17 19:18:48)

# AWS S3

### Install the Remote File Systems plugin

This functionality relies on the [Remote File Systems](https://plugins.jetbrains.com/plugin/21706-remote-file-systems) plugin, which you need to install and enable. 

The Remote File Systems plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Marketplace tab, find the Remote File Systems plugin, and click Install (restart the IDE if prompted).




### Connect to an AWS S3 server

  1. In the Big Data Tools window, click ![Add a connection](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) and select AWS S3.

  2. In the Big Data Tools dialog that opens, specify the connection parameters:

![Configure S3 connection](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_s3_connection.png)
     * Name: the name of the connection to distinguish it between the other connections.

     * Select the storage type: AWS S3 or a custom S3 compatible storage.

     * Specify the storage location:

       * For an AWS S3 storage, select the area of your storage region in the Area list.

       * For a custom S3 compatible storage, enter the endpoint URL in the Endpoint field and, optionally, enter the storage region, such as `us-east-2`.

     * Choose the way to get buckets:

       * To get specific buckets only, select Custom roots and, in the Roots field, specify the name of the bucket or the path to a directory in the bucket. You can specify multiple names or paths by separating them with a comma.

       * To get all buckets, select All buckets in the account. You can then use the bucket filter to show only buckets with particular names. You can also select Only buckets in the selected region and then select a region if you want to show buckets only from a particular region. 

     * Authentication type lets you select the authentication method:

       * Default credential providers chain: use the credentials from the default provider chain. For more information about the chain, refer to [Using the Default Credential Provider Chain](https://docs.aws.amazon.com/sdk-for-java/v1/developer-guide/credentials.html).

       * Profile from credentials file: select a profile from your credentials file.

       * Explicit access key and secret key: enter your credentials manually.

       * Anonymous: if you do not want to restrict access to a publicly visible bucket.

If you authenticate using a profile from config or credentials file, IntelliJ IDEA enables you to share your MFA or OAuth 2.0 data across all AWS connections. This means that if you select the same profile in AWS S3, AWS EMR, and AWS Glue, you don't have to perform MFA or OAuth 2.0 authentication again.

With the Default credential providers chain or Profile from credentials file option selected, you can click Open Credentials to locate the directory where the credential file is stored. If you use the default location, it's usually ~/.aws/credentials on Linux or macOS, or C:\Users\<USERNAME>\\.aws\credentials on Windows. Or it can be your custom location if you have selected Use custom configs.

Optionally, you can set up:

     * Per project: select to enable these connection settings only for the current project. Clear the checkbox if you want this connection to be visible in other projects.

     * Enable connection: clear the checkbox if you want to disable this connection. By default, the newly created connections are enabled.

You can also set up Extended Connection Settings:

     * HTTP Proxy: select if you want to use [IDE proxy settings](settings-http-proxy.html) or specify custom proxy settings.

     * Enable tunneling. This option creates an SSH tunnel to the remote host. It can be useful if the target server is in a private network but an SSH connection to the host in the network is available.

     * Operation timeout (s): enter a timeout (in seconds) for operations performed on the remote storage, such as getting file info, listing or deleting objects. The default value is 15 seconds.

     * Trust all SSL certificates: select it if you trust the SSL certificate used for this connection and do not want to verify it. This can be useful if, for development purposes, you have a host with a self-signed certificate – verifying it could result in an error.

  3. Once you fill in the settings, click Test connection to ensure that all configuration parameters are correct. Then click OK.




Once you have established a connection, you can view the storage and [work with data files](big-data-tools-data-files.html) in it.

09 May 2025

[Alibaba OSS](big-data-tools-alibaba-oss.html)[Azure](big-data-tools-azure.html)
