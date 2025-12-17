[//]: # (Source: https://www.jetbrains.com/help/idea/customizing-upload.html)
[//]: # (Downloaded: 2025-12-17 19:23:47)

# Customize upload and download

Besides the mandatory settings that ensure successful upload and download in various project – server setups, you can configure additional options to customize the interaction with the server. Most of these options apply to all server access configuration types. For FTP, FTPS, and SFTP server configurations, you can specify additional protocol-specific options.

### Enable the FTP/SFTP/WebDAV Connectivity plugin

This functionality relies on the [FTP/SFTP/WebDAV Connectivity](https://plugins.jetbrains.com/plugin/13125-ftp-sftp-webdav-connectivity) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

The FTP/SFTP/WebDAV Connectivity plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the FTP/SFTP/WebDAV Connectivity plugin, and select the checkbox next to the plugin name.




### Set common upload and download options

  1. Press `Ctrl+Alt+S` to open settings and then select Build, Execution, Deployment | Deployment | Options. 

Alternatively, go to Tools | Deployment | Options... in the main menu.

  2. Specify additional settings:

     * To skip specific files or entire folders during upload and download, in the Exclude items by name field, specify the patterns that define the names of these files and folders.

Use semicolons `;` as delimiters, asterisks `*` to match zero or more characters, and question marks `?` to match a single character.

For example, if you have a folder stylesheets with three files style.css, style1.css, and style2.scss, then `style*` excludes the entire folder, `style?.css` excludes style1.css, and `style?.*` excludes style1.css and style2.scss.

Learn more from [Regular-Expressions.info](https://www.regular-expressions.info/quickstart.html).

The exclusion is applied recursively. This means that if a matching folder has subfolders, the contents of these subfolders are not deployed either.

For more information, refer to [Exclude files and folders from uploading and downloading](excluding-files-and-folders-from-deployment.html).

     * Specify the details of the upload and download procedure by selecting or clearing the corresponding checkboxes.




### Specify additional protocol-specific customization options

  1. Press `Ctrl+Alt+S` to open settings and then select Build, Execution, Deployment | Deployment. 

Alternatively, go to Tools | Deployment | Configuration in the main menu.

  2. Select a configured server and expand the [Advanced](deployment-connection-tab.html#advanced-settings-area) group on the Connection tab to specify additional uploading settings that depend on the protocol:

     * In the Number of connections field, specify the maximum number of connections to be supported simultaneously. 

     * In the Send keep-alive messages each field, specify how often you want IntelliJ IDEA to send commands to the server to reset the timeout and thus preserve the connection. 

     * In the Encoding for client-server communication field, specify the encoding that matches the encoding used by your server. Accept the default value if you are not sure that it supports UTF-8 encoding. 

     * To set the client to the [passive mode](https://slacksite.com/other/ftp.html#passive), select the Passive mode checkbox. In this mode, the client on your machine connects to the server to inform about being in the passive mode, receives the port number to listen to, and established data connection through the port with the received number. This mode is helpful when your machine is behind a firewall. 

     * To have the hidden files and directories (with names starting with a dot .) shown in the [Server Browser Tool Window](remote-host-tool-window.html), select Show and process hidden files.

     * Select Compatible with old version of listing children in the Use LIST command area to ensure [compatibility in child file naming](https://issues.apache.org/jira/browse/VFS-310) with your FTP server. 

This option is helpful if the remote FTP server reports the following error:

Invalid descendant file name <file name>

Selecting this option may slow down synchronization with the server.

     * Select Instead of MLSD in the Use LIST command area to use the standard `LIST` command for listing instead of the `MLSD` command. This lets you avoid problems, for example, failure during upload with the Invalid descendent file name exception if the FTP server supports `MLSD` and returns `cdir`. 

     * In the Number of connections field, specify the maximum number of connections to be supported simultaneously. 

     * In the Send keep-alive messages each field, specify how often you want IntelliJ IDEA to send commands to the server to reset the timeout and thus preserve the connection. 

     * From the Keep-alive command list, choose the commands to be sent to the server to reset the timeout and thus preserve the connection. 

     * TLS: the method of Transfer Layer Security. Select Explicit to use the same port as Plain (unsecured) mode or Implicit to use a dedicated port.

     * Data channel protection level: select Clear for non-secured connection or Private for secured connection.

     * Reuse SSL session: select to reuse the security contract, including key and algorithm agreement information, established during SSL connection.

     * Disable TLS 1.3: select to disable TLS 1.3 features and have IntelliJ IDEA fall back to connecting via TLS 1.2. Use this option if you experience issues with establishing a connection to a server or uploading certain files. 

IntelliJ IDEA supports connecting to servers via TLS 1.2 and later. Using TLS 1.0 and TLS 1.1 is not supported, since these protocols [are deprecated](https://datatracker.ietf.org/doc/rfc8996/) and considered insecure. 

     * To set the client to the [passive mode](https://slacksite.com/other/ftp.html#passive), select the Passive mode checkbox. In this mode, the client on your machine connects to the server to inform about being in the passive mode, receives the port number to listen to, and established data connection through the port with the received number. This mode is helpful when your machine is behind a firewall. 

     * To have the hidden files and directories (with names starting with a dot .) shown in the [Server Browser Tool Window](remote-host-tool-window.html), select Show and process hidden files.

     * Select Compatible with old version of listing children in the Use LIST command area to ensure [compatibility in child file naming](https://issues.apache.org/jira/browse/VFS-310) with your FTP server. 

This option is helpful if the remote FTP server reports the following error:

Invalid descendant file name <file name>

Selecting this option may slow down synchronization with the server.

     * Select Instead of MLSD in the Use LIST command area to use the standard `LIST` command for listing instead of the `MLSD` command. This lets you avoid problems, for example, failure during upload with the Invalid descendent file name exception if the FTP server supports `MLSD` and returns `cdir`. 




11 October 2024

[Create a remote server configuration](creating-a-remote-server-configuration.html)[Exclude files and folders from uploading and downloading](excluding-files-and-folders-from-deployment.html)
