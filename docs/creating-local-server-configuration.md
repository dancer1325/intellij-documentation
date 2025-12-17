[//]: # (Source: https://www.jetbrains.com/help/idea/creating-local-server-configuration.html)
[//]: # (Downloaded: 2025-12-17 19:23:36)

# Create a local server configuration

A local server is a server that runs in a local or mounted folder and serves files to a local URL address. In a local server configuration, you do the development in a IntelliJ IDEA project, and then upload the project files to the document root on the server.

To create a local server configuration in IntelliJ IDEA, you need to [set up connection](#server-url) between IntelliJ IDEA and the server and [configure mapping](#mapping) between the IntelliJ IDEA project and the project folder on the server and its corresponding URL path.

### Enable the FTP/SFTP/WebDAV Connectivity plugin

This functionality relies on the [FTP/SFTP/WebDAV Connectivity](https://plugins.jetbrains.com/plugin/13125-ftp-sftp-webdav-connectivity) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

The FTP/SFTP/WebDAV Connectivity plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the FTP/SFTP/WebDAV Connectivity plugin, and select the checkbox next to the plugin name.




### 1\. Specify the name, type, and visibility of a server configuration

  1. Press `Ctrl+Alt+S` to open settings and then select Build, Execution, Deployment | Deployment. 

Alternatively, go to Tools | Deployment | Configuration in the main menu.

  2. In the left-hand pane that lists all the existing server configurations, click Add ![Add item](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select Local or mounted folder in the popup menu. 

![Add local or mounted folder](https://resources.jetbrains.com/help/img/idea/2025.3/select_local_server_type.png)
  3. In the Create new server dialog that opens, type the name of the server to create and click OK. The Create new server dialog closes and you return to the [Connection](deployment-connection-tab.html) tab of the [Deployment](settings-deployment.html) node.

  4. From the list of servers, select the one you want to make default and click ![the Use as default button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.setDefault.svg) Use as Default on the toolbar above the list of servers to [mark the server as default](configuring-synchronization-with-a-remote-host.html#default_server). 

  5. Clear the Visible only for this project checkbox to enable reuse of this server access configuration in other projects. 

The server configuration settings are stored in the .idea directory together with the project, which allows sharing them between team members [through a VCS](version-control-integration.html).




### 2\. Set up connection to the server

In the Connection tab (`Ctrl+Alt+S` | Build, Execution, Deployment | Deployment), specify the server settings:

  * Folder: specify the absolute path to the server document root as defined in your server configuration file. Besides the document root itself, any other existing folder under the document root can also be specified. 

The document root is the folder from which the web server serves files to the web server URL.

Examples:

    *     * `/var/www/html` or `/usr/local/apache/htdocs` for a standalone locally installed Apache server.

  * Web server URL: the URL address (hostname and (optionally) port) mapped to the server document root in the server configuration file. This is the base URL for your application's web address. Both HTTP and HTTPS are supported. 

Examples:

    * `http://localhost:80`

    * `http://localhost:80/MySite1` (if you choose to establish a more complicated folder structure under the server document root and use only one of the subfolders in the current configuration)

Click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.toolwindow.web.svg) Browse in the right-hand corner of the field to open and check the provided web server URL.




### 3\. Map project folder to a server folder and URL path

In the Mappings tab (`Ctrl+Alt+S` | Build, Execution, Deployment | Deployment), specify the mapping between the project opened in IntelliJ IDEA and the folder under the server document root that shall correspond to it:

![Deployment Mappings tab](https://resources.jetbrains.com/help/img/idea/2025.3/deployment_mappings_tab.png)

  * Local path: the absolute path to the local project folder. IntelliJ IDEA automatically fills out this field with the path to the currently opened project. 

  * Deployment path: a folder under the server document root where IntelliJ IDEA will upload the contents of the project folder specified in the Local path field. 

Deployment path is relative to the Folder path specified in the Connection tab.

If a folder with the specified name does not yet exist on the server, IntelliJ IDEA will create it when you trigger [project upload](uploading-and-downloading-files.html#manually).

The easiest way is to map the entire project root folder to a folder under the server document root. The project folder structure in this case will be recreated on the server. 

  * Web path: the URL path configured for the folder specified in Deployment path. You can use a slash (`/`) to point to the root folder, or leave the field blank if the directory is not accessible from the web. 

Web path is relative to the Web server URL specified in the Connection tab.




Example:

  * Local path: `Users/John.Smith/demo-project`

  * Deployment path: `/my-project`

  * Web path: `/my-project`




Now that you have the server configuration added, you can access the server's files and folders in the [Remote Host tool window](remote-host-tool-window.html). Go to Tools | Deployment | Browse Remote Host in the main menu, and in the tool window that opens, select the configured server from the drop-down list.

![Open the Remote Host tool window and select the server](https://resources.jetbrains.com/help/img/idea/2025.3/select_server_in_remote_host_tool_window.png)

08 October 2024

[Create an in-place server configuration](creating-in-place-server-configuration.html)[Create a remote server configuration](creating-a-remote-server-configuration.html)
