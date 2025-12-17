[//]: # (Source: https://www.jetbrains.com/help/idea/editing-individual-files-on-remote-hosts.html)
[//]: # (Downloaded: 2025-12-17 19:25:36)

# Edit individual files on remote hosts

Once you have [set up synchronization](configuring-synchronization-with-a-remote-host.html) with a remote host, you can open individual files directly from the remote host and edit them in IntelliJ IDEA, without adding/downloading them to a local project.

Debugging, refactorings, and some other IntelliJ IDEA features are not supported for such files. To take advantage of advanced IntelliJ IDEA functionality, consider including the files in a project. For more information, refer to [Access files on servers](accessing-files-on-remote-hosts.html).

### Enable the FTP/SFTP/WebDAV Connectivity plugin

This functionality relies on the [FTP/SFTP/WebDAV Connectivity](https://plugins.jetbrains.com/plugin/13125-ftp-sftp-webdav-connectivity) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

The FTP/SFTP/WebDAV Connectivity plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the FTP/SFTP/WebDAV Connectivity plugin, and select the checkbox next to the plugin name.




### Edit a file on a remote host

  1. If you have set a [default remote host](configuring-synchronization-with-a-remote-host.html#default_server), select Deployment | Edit Remote File from the context menu in the [Project tool window](project-tool-window.html), Commit tool window `Alt+0`, or the code editor.

Otherwise, do the following:

     1. Open the [Remote Host tool window](remote-host-tool-window.html) by choosing Tools | Deployment | Browse Remote Host or View | Tool Windows | Remote Host from the main menu. 

     2. Select the required deployment server from the list. The tool window shows a tree view of files and folders under the server root. If no relevant server is available in the list, click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg), and in the Deployment dialog that opens [configure access to the required server](configuring-synchronization-with-a-remote-host.html). 

     3. Double-click the desired file or select Edit Remote File from the context menu.

![Edit file on remote host](https://resources.jetbrains.com/help/img/idea/2025.3/ij_edit_file_on_remote_host.png)
  2. The file opens in the IntelliJ IDEA editor, without being added or downloaded to the local project.

![Editing a file on remote host](https://resources.jetbrains.com/help/img/idea/2025.3/ij_edit_file_on_remote_host_1.png)

When you work with a remote file, a special toolbar appears at the top of the editor, showing the editing status (The file is identical to remote one or The file has been modified. Upload?).

Remote files can be distinguished from local ones by the annotation that includes the server name (in our case, it is <MyServer>) .

![Remote file annotation](https://resources.jetbrains.com/help/img/idea/2025.3/ij_edit_file_on_remote_host_2.png)
  3. When you are done editing the file, do one of the following:

     * To upload the file to the remote host, click ![the Upload current remote file button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.upload.svg) or press `Alt+Shift+Q`.

     * To compare the currently opened file with the last uploaded version, click ![the Compare with last uploaded version button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.vcs.diff.svg). The files are opened in the IntelliJ IDEA [Diff Viewer for files](differences-viewer.html).

     * To discard the changes introduced to the file after the last upload, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.vcs.revert.svg).




Note that any changes to an individual file are discarded as soon as you close the file or the currently opened project unless these changes have been uploaded. To prevent losing your data, IntelliJ IDEA displays the following dialog when you attempt to close the edited file or the entire project.

![Confirm uploading message](https://resources.jetbrains.com/help/img/idea/2025.3/ij_edit_file_on_remote_host_3.png)

10 December 2025

[Compare deployed files and folders with their local versions](comparing-deployed-files-and-folders-with-their-local-versions.html)[Create SSH configurations](create-ssh-configurations.html)
