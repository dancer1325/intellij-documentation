[//]: # (Source: https://www.jetbrains.com/help/idea/big-data-tools-local-file-system.html)
[//]: # (Downloaded: 2025-12-17 19:19:10)

# Local file system

### Install the Remote File Systems plugin

This functionality relies on the [Remote File Systems](https://plugins.jetbrains.com/plugin/21706-remote-file-systems) plugin, which you need to install and enable. 

The Remote File Systems plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Marketplace tab, find the Remote File Systems plugin, and click Install (restart the IDE if prompted).




### Connect to a local file system

  1. In the Big Data Tools window, click ![Add a connection](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) and select Local.

  2. In the Big Data Tools dialog that opens, specify the connection parameters:

![Local FS](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_local_fs_connection.png)
     * Name: the name of the connection to distinguish it between the other connections.

     * Root path: a path to the root directory.

Optionally, you can set up:

     * Per project: select to enable these connection settings only for the current project. Clear the checkbox if you want this connection to be visible in other projects.

     * Enable connection: clear the checkbox if you want to disable this connection. By default, the newly created connections are enabled.

  3. Once you fill in the settings, click Test connection to ensure that all configuration parameters are correct. Then click OK.




09 May 2025

[SFTP](big-data-tools-sftp.html)[Work with data files](big-data-tools-data-files.html)
