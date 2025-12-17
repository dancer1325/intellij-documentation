[//]: # (Source: https://www.jetbrains.com/help/idea/deploying-applications.html)
[//]: # (Downloaded: 2025-12-17 19:24:37)

## Interaction between IntelliJ IDEA and servers

Interaction between IntelliJ IDEA and servers is controlled through server access configurations. Anytime you are going to use a server, you need to define a server access configuration, no matter whether your server is on a remote host or on your computer.

Taking into account all the above, let's define the following basic concepts related to synchronization between IntelliJ IDEA and servers.

  * In-place server configuration.

In an in-place server configuration, you are using a local web server, but unlike with the [local server configuration](creating-local-server-configuration.html), don't upload/download or synchronize files between the IntelliJ IDEA project and the project folder in the server file structure. Instead, you open the project folder from the server document root directly in IntelliJ IDEA, and thus do the development on the server directly.

[Create an in-place server configuration](creating-in-place-server-configuration.html)

  * Local server configuration.

A local server is a server that runs in a local or mounted folder and serves files to a local URL address. In a local server configuration, you do the development in a IntelliJ IDEA project, and then upload the project files to the document root on the server.

[Create a local server configuration](creating-local-server-configuration.html)

  * Remote server configuration.

In a remote server configuration, the server runs on another computer (a remote host). To access files on the remote server, use FTP/SFTP/FTPS/WebDAV protocols.

[Create a remote server configuration](creating-a-remote-server-configuration.html)

  * The server configuration root is the highest folder in the file tree on the local or remote server accessible through the server configuration. For in-place servers, it is the project root.

  * A local file/folder is any file or folder under the project root.

  * A remote file/folder is any file or folder on the server.

  * Upload is copying data from the project TO the server, either local or remote.

  * Download is copying data FROM the server to the project.




After you have configured synchronization with a server, you can upload, download, and manage files on it directly from IntelliJ IDEA. Moreover, you can suppress uploading or downloading specific files or entire folders. Finally, you can optimize your workflow by configuring content roots so specific folders are not involved in indexing, which significantly saves project indexing time.

Synchronization with servers, uploading, downloading, and managing files on them are provided via the FTP/SFTP/WebDAV Connectivity bundled plugin, which is by default enabled. If the plugin is disabled, activate it in the Plugins page of the Settings dialog. For more information, refer to [Install plugins](managing-plugins.html). Note that the plugin is available only in IntelliJ IDEA with the Ultimate subscription. 
