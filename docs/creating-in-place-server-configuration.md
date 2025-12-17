[//]: # (Source: https://www.jetbrains.com/help/idea/creating-in-place-server-configuration.html)
[//]: # (Downloaded: 2025-12-17 19:23:33)

# Create an in-place server configuration

In an in-place server configuration, you are using a local web server, but unlike with the [local server configuration](creating-local-server-configuration.html), don't upload/download or synchronize files between the IntelliJ IDEA project and the project folder in the server file structure. Instead, you open the project folder from the server document root directly in IntelliJ IDEA, and thus do the development on the server directly.

To create an in-place server configuration in IntelliJ IDEA, you only need to specify the [web server URL](#server-url) mapped to the server document root and the [URL path to your project](#project-root-folder).

### Enable the FTP/SFTP/WebDAV Connectivity plugin

This functionality relies on the [FTP/SFTP/WebDAV Connectivity](https://plugins.jetbrains.com/plugin/13125-ftp-sftp-webdav-connectivity) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

The FTP/SFTP/WebDAV Connectivity plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the FTP/SFTP/WebDAV Connectivity plugin, and select the checkbox next to the plugin name.




### 1\. Specify the name, type, and visibility of a server configuration

  1. Press `Ctrl+Alt+S` to open settings and then select Build, Execution, Deployment | Deployment. 

Alternatively, go to Tools | Deployment | Configuration in the main menu.

  2. In the left-hand pane that lists all the existing server configurations, click Add ![Add item](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select In place in the popup menu.

![Add in-place server configuration](https://resources.jetbrains.com/help/img/idea/2025.3/select_inplace_server_type.png)
  3. In the Create new server dialog that opens, type the name of the server to create and click OK. The Create new server dialog closes and you return to the [Connection](deployment-connection-tab.html) tab of the [Deployment](settings-deployment.html) node.

  4. From the list of servers, select the one you want to make default and click ![the Use as default button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.setDefault.svg) Use as Default on the toolbar above the list of servers to [mark the server as default](configuring-synchronization-with-a-remote-host.html#default_server). 

  5. Clear the Visible only for this project checkbox to enable reuse of this server access configuration in other projects. 

The server configuration settings are stored in the .idea directory together with the project, which allows sharing them between team members [through a VCS](version-control-integration.html).




### 2\. Specify the URL address of the server document root

In the Connection tab (`Ctrl+Alt+S` | Build, Execution, Deployment | Deployment), specify:

  * Web server URL: the URL address (hostname and (optionally) port) mapped to the server document root in the server configuration file. This is the base URL for your application's web address. Both HTTP and HTTPS are supported. 

Examples:

    * `http://localhost:80`

    * `http://localhost:80/MySite1` (if you choose to establish a more complicated folder structure under the server document root and use only one of the subfolders in the current configuration)

Click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.toolwindow.web.svg) Browse in the right-hand corner of the field to open and check the provided web server URL.




### 3\. Specify the URL path mapped to the project folder

In the Mappings tab (`Ctrl+Alt+S` | Build, Execution, Deployment | Deployment), specify:

![Deployment Mappings tab](https://resources.jetbrains.com/help/img/idea/2025.3/deployment_mappings_tab_inplace_server.png)

  * Local path: the absolute path to the local project folder. IntelliJ IDEA automatically fills out this field with the path to the currently opened project. 

  * Web path: the URL path to the project folder specified in Local path. In most cases, it's the same as the folder name provided in the Local path field.

IntelliJ IDEA appends Web path to the Web server URL specified in the [Connection tab](#server-url).




Example:

  * Local path: `Users/John.Smith/demo-project`

  * Web path: `/demo-project`




Now that you have the server configuration added, you can access the server's files and folders in the [Remote Host tool window](remote-host-tool-window.html). Go to Tools | Deployment | Browse Remote Host in the main menu, and in the tool window that opens, select the configured server from the drop-down list.

![Open the Remote Host tool window and select the server](https://resources.jetbrains.com/help/img/idea/2025.3/select_server_in_remote_host_tool_window.png)

08 October 2024

[Connect to a web server](configuring-synchronization-with-a-remote-host.html)[Create a local server configuration](creating-local-server-configuration.html)
