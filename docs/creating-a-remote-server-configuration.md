[//]: # (Source: https://www.jetbrains.com/help/idea/creating-a-remote-server-configuration.html)
[//]: # (Downloaded: 2025-12-17 19:23:14)

# Create a remote server configuration

In a remote server configuration, the server runs on another computer (a remote host). To access files on the remote server, use FTP/SFTP/FTPS/WebDAV protocols.

### Enable the FTP/SFTP/WebDAV Connectivity plugin

This functionality relies on the [FTP/SFTP/WebDAV Connectivity](https://plugins.jetbrains.com/plugin/13125-ftp-sftp-webdav-connectivity) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

The FTP/SFTP/WebDAV Connectivity plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the FTP/SFTP/WebDAV Connectivity plugin, and select the checkbox next to the plugin name.




To create a remote server configuration in IntelliJ IDEA, you need to:

  1. [Authenticate with the remote host and set up connection](#server-url) between the web server installed on it and IntelliJ IDEA.

  2. [Configure mapping](#mapping) between the IntelliJ IDEA project and the project folder on the host and its corresponding URL path.




### 1\. Specify the name, type, and visibility of a server configuration

  1. Press `Ctrl+Alt+S` to open settings and then select Build, Execution, Deployment | Deployment. 

Alternatively, go to Tools | Deployment | Configuration in the main menu.

  2. In the left-hand pane that lists all the existing server configurations, click ![Add item](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select the server configuration type depending on the protocol you are going to use to exchange the data with the server.

     * FTP: choose this option to have IntelliJ IDEA access the server via the FTP [file transfer protocol](https://en.wikipedia.org/wiki/File_Transfer_Protocol).

     * SFTP: choose this option to have IntelliJ IDEA access the server via the [SFTP](https://en.wikipedia.org/wiki/SFTP) file transfer protocol.

     * FTPS: choose this option to have IntelliJ IDEA access the server via the FTP file transfer protocol over SSL (the [FTPS](https://en.wikipedia.org/wiki/FTPS) extension).

     * WebDAV: choose this option to have IntelliJ IDEA access the server via the WebDAV file transfer protocol (the [WebDAV](https://en.wikipedia.org/wiki/WebDAV) extension).

  3. In the Create New Server dialog that opens, type the name of the connection to the server and click OK. The Create New Server dialog closes and you return to the [Connection](deployment-connection-tab.html) tab of the [Deployment](settings-deployment.html) node. 

  4. From the list of servers, select the one you want to make default and click ![the Use as default button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.setDefault.svg) Use as Default on the toolbar above the list of servers to [mark the server as default](configuring-synchronization-with-a-remote-host.html#default_server). 

  5. Clear the Visible only for this project checkbox to enable reuse of this server access configuration in other projects. 

The server configuration settings are stored in the .idea directory together with the project, which allows sharing them between team members [through a VCS](version-control-integration.html).




### 2\. Set up connection to the remote host and its server

In the Connection tab (`Ctrl+Alt+S` | Build, Execution, Deployment | Deployment), specify settings for the remote host access, files transfer parameters, and the web server configuration:

  1. Specify the host address, port, and user credentials to access it. The required fields differ depending on the used protocol type.

![Create remote host SFTP connection](https://resources.jetbrains.com/help/img/idea/2025.3/remote-host-sftp.png)
     * SSH configuration: select one of the previously created SSH configurations from the list, or click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and create a new configuration as described in [Create SSH configurations](create-ssh-configurations.html).

     * Use rsync for download/upload/sync: select the checkbox to have IntelliJ IDEA use [Rsync](https://rsync.samba.org) for uploading and downloading files, which can increase file transfer speeds. 

Click Rsync Settings to open the [Rsync settings page](settings-tools-rsync.html) and configure Rsync.

![Create remote host FTP, FTPS, WebDav connection](https://resources.jetbrains.com/help/img/idea/2025.3/remote-host-ftp.png)
     * Host: specify the hostname of the server to exchange data with.

     * Port: specify the port to which this server listens. The FTP/FTPS, the default value is `21`. For WebDAV, the default value is `6180`.

     * Username and Password: provide the username and password specified during registration on the host.

Select the Save password checkbox to store the password in IntelliJ IDEA permanently (otherwise, it will only be stored until the IDE restart).

Or, alternatively, select the Login as anonymous checkbox to enable anonymous authentication with the server and use the email address as a password.

  2. Set up a connection to the remote host's web server:

     * Root path: specify the folder used as the remote directory root for browsing the remote file system and setting the server path mappings and excluded paths. 

Do one of the following:

       * Accept the default `/` path, which points at the root folder on the server.

       * Type the path manually or click ![Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.open.svg) and select the desired folder in the Choose Root Path dialog that opens.

       * Click Autodetect. IntelliJ IDEA detects the user home folder settings on the FTP/SFTP server and sets up the root path according to them. The button is only enabled when you have specified your credentials.

     * Web server URL: specify the URL address configured for the folder specified in Root path. Both HTTP and HTTPS are supported. 

Click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.toolwindow.web.svg) Browse in the right-hand corner of the field to open and check the provided web server URL.

  3. (Optional) Expand the Advanced section to configure more settings as described in:

     * [SFTP advanced settings](deployment-connection-tab.html#sftp-advanced-settings)

     * [FTP and FTPS advanced settings](deployment-connection-tab.html#advanced-settings-area)




### 3\. Map project folder to a server folder and URL path

In the Mappings tab (`Ctrl+Alt+S` | Build, Execution, Deployment | Deployment), specify:

  1. Local path: the absolute path to the local project folder. IntelliJ IDEA automatically fills out this field with the path to the currently opened project. 

  2. Deployment path: a folder under the server root where IntelliJ IDEA will upload the contents of the project folder specified in the Local path field.

Deployment path is relative to the Root path specified in the Connection tab.

If a folder with the specified name does not yet exist on the server, IntelliJ IDEA will create it when you trigger [project upload](uploading-and-downloading-files.html#manually).

  3. Web path: the URL path configured for the folder specified in Deployment path. You can use a slash (`/`) to point to the root folder, or leave the field blank if the directory is not accessible from the web. 

Web path is relative to the Web server URL specified in the Connection tab.




There are cases when you might want to add several mappings per project. For example, you can overwrite the destination folder on the server for a specific `nested-folder` in the IntelliJ IDEA project by adding a separate mapping for it:

![Example of advanced remote server mapping](https://resources.jetbrains.com/help/img/idea/2025.3/remote_server_mapping_example.png)

In this case, `Users/John.Smith/demo-project/nested-folder` will be uploaded to `/root-path/nested-folder` on the server, while all other folders and files from `/demo-project` will still map to `/root-path/my-site`.

Now that you have the server configuration added, you can access the server's files and folders in the [Remote Host tool window](remote-host-tool-window.html). Go to Tools | Deployment | Browse Remote Host in the main menu, and in the tool window that opens, select the configured server from the drop-down list.

![Open the Remote Host tool window and select the server](https://resources.jetbrains.com/help/img/idea/2025.3/select_server_in_remote_host_tool_window.png)

01 August 2025

[Create a local server configuration](creating-local-server-configuration.html)[Customize upload and download](customizing-upload.html)
