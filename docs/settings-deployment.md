[//]: # (Source: https://www.jetbrains.com/help/idea/settings-deployment.html)
[//]: # (Downloaded: 2025-12-17 20:00:51)

## Toolbar icons and context menu commands

Use the toolbar buttons and context menu commands to manage the list of configurations and server groups.

The left-hand pane shows a list of all the server access configurations and server groups available in IntelliJ IDEA. When you select an item, the right-hand pane shows the configuration details.

Item| Tooltip and shortcut| Description  
---|---|---  
![Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| Add`Insert`| Click this button and select the desired item from the list to define a new configuration or server group. The following options are available:

  * FTP: choose this option to have IntelliJ IDEA access the server via the FTP [file transfer protocol](https://en.wikipedia.org/wiki/File_Transfer_Protocol).
  * SFTP: choose this option to have IntelliJ IDEA access the server via the [SFTP](https://en.wikipedia.org/wiki/SFTP) file transfer protocol.
  * FTPS: choose this option to have IntelliJ IDEA access the server via the FTP file transfer protocol over SSL (the [FTPS](https://en.wikipedia.org/wiki/FTPS) extension).
  * WebDAV: choose this option to have IntelliJ IDEA access the server via the WebDAV file transfer protocol (the [WebDAV](https://en.wikipedia.org/wiki/WebDAV) extension).
  * Server group: choose this option to create a [server group](server-groups.html), which lets you group server configurations together and work with them as with a single entity.

  
![Remove button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| `Delete`| Click this button to remove the selected configuration or server group from the list. Note that removing a server group also removes the contained servers.  
![icon_use_web_server_configuration_as_default](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.setDefault.svg)| Use as Default| Click this button to have IntelliJ IDEA apply the settings of the selected configuration or server group by default during automatic upload of changed files.  
![Duplicate button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.copy.svg)| Duplicate`Ctrl+D`| Select this command from the context menu to duplicate the selected configuration or server group.  
| Rename`Shift+F6`| Select this command from the context menu to rename the selected configuration or server group.
