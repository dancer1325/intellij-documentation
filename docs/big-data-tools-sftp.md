[//]: # (Source: https://www.jetbrains.com/help/idea/big-data-tools-sftp.html)
[//]: # (Downloaded: 2025-12-17 19:19:13)

# SFTP

### Install the Remote File Systems plugin

This functionality relies on the [Remote File Systems](https://plugins.jetbrains.com/plugin/21706-remote-file-systems) plugin, which you need to install and enable. 

The Remote File Systems plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Marketplace tab, find the Remote File Systems plugin, and click Install (restart the IDE if prompted).




### Connect to an SFTP server

  1. In the Big Data Tools window, click ![Add a connection](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) and select SFTP.

  2. In the Big Data Tools dialog that opens, specify the connection parameters:

![HDFS connection](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_sftp_fs_connection.png)
     * Name: the name of the connection to distinguish it between the other connections.

     * SSH configuration: select an [SSH configuration](create-ssh-configurations.html), which contains the needed server address and credentials.

     * Root path: a path to the root directory.

Optionally, you can set up:

     * Per project: select to enable these connection settings only for the current project. Clear the checkbox if you want this connection to be visible in other projects.

     * Enable connection: clear the checkbox if you want to disable this connection. By default, the newly created connections are enabled.

     * Use sudo to run SFTP server: select if your target server requires root access. With this option selected, you will be prompted to enter a root user password while connecting to the SFTP server.

     * Use custom command to start SFTP server: select if you want to customize the server startup command. With this option selected, the following parameters become available:

       * Command to start SFTP server: enter a path to the SFTP server or provide SFTP connection options. If the Use sudo to run SFTP server option is selected, you can leave the field empty and let IntelliJ IDEA detect the path to the SFTP server. Click Test connection to view the detected path.

       * Suggest using sudo for files with restricted permission: with the option selected, IntelliJ IDEA will ask if you want to use the sudo password each time you try to read or write files with restricted access. If not selected, accessing such files will result in the "Permission denied" error. The option is available if Use sudo to run SFTP server is not selected.

       * Use password from SSH configuration: select if, for accessing files, you want to use the password provided by the selected [SSH configuration](create-ssh-configurations.html). If the password is empty or if Authentication type of the SSH configuration is not Password, IntelliJ IDEA will require you to enter a password while running the server and accessing files.

The option is available if Use sudo to run SFTP server or Suggest using sudo for files with restricted permission is selected.

       * Command to run sudo: customize the sudo command; for example, you can enter the full path to sudo or provide options such as `sudo -k`.

  3. Once you fill in the settings, click Test connection to ensure that all configuration parameters are correct. Then click OK.




09 May 2025

[HDFS](big-data-tools-hdfs.html)[Local file system](big-data-tools-local-file-system.html)
