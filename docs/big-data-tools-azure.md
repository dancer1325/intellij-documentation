[//]: # (Source: https://www.jetbrains.com/help/idea/big-data-tools-azure.html)
[//]: # (Downloaded: 2025-12-17 19:18:49)

# Azure

### Install the Remote File Systems plugin

This functionality relies on the [Remote File Systems](https://plugins.jetbrains.com/plugin/21706-remote-file-systems) plugin, which you need to install and enable. 

The Remote File Systems plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Marketplace tab, find the Remote File Systems plugin, and click Install (restart the IDE if prompted).




### Connect to Microsoft Azure

  1. In the Big Data Tools window, click ![Add a connection](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) and select Azure.

  2. In the Big Data Tools dialog that opens, specify the connection parameters:

![Connection settings for Azure Storage](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_azure.png)
     * Name: the name of the connection to distinguish it between the other connections.

     * Authentication type: select the authentication method.

       * Azure Account: click Authenticate to get your Azure authentication data. In the windows that opens, select one of the following:

         * Azure CLI (available if [you have signed in to Azure CLI](https://learn.microsoft.com/en-us/cli/azure/authenticate-azure-cli)).

         * OAuth2: open your default browser to complete Azure authentication.

         * Device code: this will open a window display a device code. Click Copy Code and Open Browser to open your default browser and enter the displayed code there.

       * Username: enter your Azure endpoint, username, and the account key.

       * Connection String: enter your Azure [connection string](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

       * SAS Token: enter your Azure endpoint and [SAS token](https://docs.microsoft.com/en-us/azure/storage/common/storage-sas-overview).

     * Choose the way to get Microsoft Azure containers:

       * Select Custom roots and, in the Container field, specify the name of the container or the path to a directory in the container. You can specify multiple names or paths by separating them with a comma.

       * Select All containers in the account. You can then use the container filter to show only containers with particular names.

Optionally, you can set up:

     * Per project: select to enable these connection settings only for the current project. Clear the checkbox if you want this connection to be visible in other projects.

     * Enable connection: clear the checkbox if you want to disable this connection. By default, the newly created connections are enabled.

  3. Once you fill in the settings, click Test connection to ensure that all configuration parameters are correct. Then click OK.




Once you have established a connection, you can view the storage and [work with data files](big-data-tools-data-files.html) in it.

07 October 2025

[AWS S3](big-data-tools-aws-s3.html)[Cloudflare R2](big-data-tools-cloudflare-r2.html)
