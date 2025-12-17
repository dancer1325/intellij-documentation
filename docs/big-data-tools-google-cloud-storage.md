[//]: # (Source: https://www.jetbrains.com/help/idea/big-data-tools-google-cloud-storage.html)
[//]: # (Downloaded: 2025-12-17 19:19:01)

# Google Cloud Storage

### Install the Remote File Systems plugin

This functionality relies on the [Remote File Systems](https://plugins.jetbrains.com/plugin/21706-remote-file-systems) plugin, which you need to install and enable. 

The Remote File Systems plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Marketplace tab, find the Remote File Systems plugin, and click Install (restart the IDE if prompted).




### Connect to Google Cloud Storage

  1. In the Big Data Tools window, click ![Add a connection](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) and select Google Cloud Storage.

  2. In the Big Data Tools dialog that opens, specify the connection parameters:

![Connection settings for Google Cloud Storage](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_gs_connection.png)
     * Name: the name of the connection to distinguish it between the other connections.

     * Choose the way to get buckets:

       * To get specific buckets only, select Custom roots and, in the Roots field, specify the name of the bucket or the path to a directory in the bucket. You can specify multiple names or paths by separating them with a comma.

       * To get all buckets, select All buckets in the account. You can then use the bucket filter to show only buckets with particular names. 

     * In the Authentication type list, select an authentication method:

       * GCloud Account: this will open your browser where you can sign in to your Google account. Once authenticated, select the Project ID.

       * Credential File: enter a path to the credential JSON file.

       * Anonymous: select if you want to sign in anonymously, for example, to public buckets.

Optionally, you can set up:

     * Per project: select to enable these connection settings only for the current project. Clear the checkbox if you want this connection to be visible in other projects.

     * Enable connection: clear the checkbox if you want to disable this connection. By default, the newly created connections are enabled.

     * Proxy: select if you want to use [IDE proxy settings](settings-http-proxy.html) or if you want to specify custom proxy settings.

     * Extended Connection Settings | Custom host: enter your custom endpoint URL, for example, if you want to use it to mock a Google Cloud Storage server.

  3. Once you fill in the settings, click Test connection to ensure that all configuration parameters are correct. Then click OK.




Once you have established a connection, you can view the storage and [work with data files](big-data-tools-data-files.html) in it.

07 October 2025

[DigitalOcean Spaces](big-data-tools-digitalocean-spaces.html)[Linode](big-data-tools-linode.html)
