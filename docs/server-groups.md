[//]: # (Source: https://www.jetbrains.com/help/idea/server-groups.html)
[//]: # (Downloaded: 2025-12-17 20:00:09)

# Organize servers into groups

Server groups let you group server configurations together and work with them as with a single entity. If you need to deploy code to multiple servers, you can use a server group and avoid deploying to each server individually.

### Enable the FTP/SFTP/WebDAV Connectivity plugin

This functionality relies on the [FTP/SFTP/WebDAV Connectivity](https://plugins.jetbrains.com/plugin/13125-ftp-sftp-webdav-connectivity) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

The FTP/SFTP/WebDAV Connectivity plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the FTP/SFTP/WebDAV Connectivity plugin, and select the checkbox next to the plugin name.




### Create a server group

  1. Press `Ctrl+Alt+S` to open settings and then select Build, Execution, Deployment | Deployment. 

Alternatively, go to Tools | Deployment | Configuration in the main menu.

  2. In the left-hand pane that lists all the existing server configurations, click Add ![Add item](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select Server group in the popup menu.

  3. In the Create new group dialog that opens, type the name of the group to be created and click OK. The Create new group dialog closes and you return to the [Connection](deployment-connection-tab.html) tab of the [Deployment](settings-deployment.html) node.

  4. To create a new server configuration inside the group, select the group in the left-hand pane and click either the Add new server link in the right-hand pane or the ![Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) toolbar button. Then configure the newly created server depending on its type as described in [Connect to a web server](configuring-synchronization-with-a-remote-host.html).

To add an existing server configuration to the group, drag it into the group. To remove a server configuration, drag it out of the group.

![Populating a server group](https://resources.jetbrains.com/help/img/idea/2025.3/ps_add_remove_servers_server_group.png)
  5. From the list of servers, select the one you want to make default and click ![the Use as default button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.setDefault.svg) Use as Default on the toolbar above the list of servers to [mark the server as default](configuring-synchronization-with-a-remote-host.html#default_server). 

  6. Use the For current project checkbox to configure the server group visibility, which also applies to all servers contained in the group.

     * Select the checkbox to restrict the use of the group to the current project. Such group cannot be reused outside the current project. It does not appear in the list of available configurations in other projects. 

     * When the checkbox is cleared, the group is visible in all IntelliJ IDEA projects. Its settings can be reused across several projects. 




The created server group can now be used for [uploading and downloading files](uploading-and-downloading-files.html) to the contained servers.

08 October 2024

[Exclude files and folders from uploading and downloading](excluding-files-and-folders-from-deployment.html)[Access files on servers](accessing-files-on-remote-hosts.html)
