[//]: # (Source: https://www.jetbrains.com/help/idea/deployment-connection-tab.html)
[//]: # (Downloaded: 2025-12-17 19:24:38)

## Common settings for all server types

Item| Description  
---|---  
Visible only for this project| Use this checkbox to enable reuse of this server access configuration or server group in other projects. 

  * Select the checkbox to restrict the use of the configuration or server group to the current project. Such configuration or server group cannot be reused outside the current project. It does not appear in the list of available configurations in other projects. The server configuration settings are stored in the .idea directory together with the project, which allows sharing them between team members [through a VCS](version-control-integration.html).In the list of server access configurations in the left-hand pane, the configurations visible only in the current project are marked with the ![Visible only in current project icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.projectConfigurable.svg) icon. 
  * When the checkbox is cleared, the configuration or server group is visible in all IntelliJ IDEA projects. Its settings can be reused across several projects. 

For more information about setting up interpreters, refer to [Node.js via SSH](node-via-ssh.html) and [Configure remote PHP interpreters](https://www.jetbrains.com/help/phpstorm/configuring-remote-interpreters.html).   
Type| In this list, choose the way to access the server. The available options are:

  * FTP: choose this option to have IntelliJ IDEA access the server via the FTP [file transfer protocol](https://en.wikipedia.org/wiki/File_Transfer_Protocol).
  * SFTP: choose this option to have IntelliJ IDEA access the server via the [SFTP](https://en.wikipedia.org/wiki/SFTP) file transfer protocol.
  * FTPS: choose this option to have IntelliJ IDEA access the server via the FTP file transfer protocol over SSL (the [FTPS](https://en.wikipedia.org/wiki/FTPS) extension).
  * WebDAV: choose this option to have IntelliJ IDEA access the server via the WebDAV file transfer protocol (the [WebDAV](https://en.wikipedia.org/wiki/WebDAV) extension).

  
Web server URL| In this field, specify the URL address that corresponds to the server document directory as specified in the server configuration file. Click ![Open URL in browser icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.toolwindows.webToolWindow.svg) in the field to make sure the specified server root URL address is accessible and points at the correct web page.Both HTTP and HTTPS are supported. 
