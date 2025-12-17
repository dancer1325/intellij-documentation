[//]: # (Source: https://www.jetbrains.com/help/idea/uploading-and-downloading-files.html)
[//]: # (Downloaded: 2025-12-17 20:05:13)

# Upload and download files

IntelliJ IDEA provides the following two ways to upload project files and folders to the [configured deployment servers](configuring-synchronization-with-a-remote-host.html):

  * Manually, at any time through a menu command.

  * Automatically, every time a file is updated, or before starting a debugging session, or during a commit to your version control system.




To mitigate the risk of temporary data loss during upload of new versions of existing files, IntelliJ IDEA can store the contents of the uploaded file under a temporary name, and only rename it back after the upload operation has been successfully completed.

To enable this option, go to Settings (`Ctrl+Alt+S`) |Build, Execution, Deployment | Deployment | Options and select the  Use a temporary file during upload checkbox.

For downloading files and folders, IntelliJ IDEA supports only the manual mode.

IntelliJ IDEA shows the logs in the File Transfer tool window.

![File Transfer tool window](https://resources.jetbrains.com/help/img/idea/2025.3/ij_file_transfer_tab.png)

### Enable the FTP/SFTP/WebDAV Connectivity plugin

This functionality relies on the [FTP/SFTP/WebDAV Connectivity](https://plugins.jetbrains.com/plugin/13125-ftp-sftp-webdav-connectivity) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

The FTP/SFTP/WebDAV Connectivity plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the FTP/SFTP/WebDAV Connectivity plugin, and select the checkbox next to the plugin name.




### Upload a file or folder manually

  * In the Project tool window (`Alt+1`), right-click a file or folder, then select Deployment | Upload to from the context menu, and choose the target deployment server or server group from the list.

![Upload file or folder manually](https://resources.jetbrains.com/help/img/idea/2025.3/upload_file_folder_manually.png)

If the default server or server group is appointed, you can also select Upload to <default deployment server or server group>.




### Upload locally changed files

  1. Switch to the Commit window (`Alt+0`) to view the locally changed files.

  2. Right-click a file, then select Deployment | Upload to from the context menu, and choose the target deployment from the list. If the default group is appointed, you can also select Upload to <default deployment >.




For more information, refer to [Add files to Git and track changes](adding-files-to-version-control.html).

### Upload files after synchronizing with a VCS repository

  1. Synchronize the contents of your local files with the VCS repository by pressing `Ctrl+T` or selecting VCS | <VCS> | Update from the main menu.

  2. Switch to the [Update Info](version-control-tool-window-update-info-tab.html) tab of the Version Control tool window `Alt+9`.

  3. Right-click a file, then select Deployment | Upload to from the context menu, and choose the target deployment from the list. If the default is appointed, you can also select Upload to <default deployment >.




### Upload checked-in files immediately after commit

  1. In the Commit window (`Alt+0`), click ![the gear icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.gear.svg) to open the commit setting context menu.

  2. In the After Commit area of the menu, choose the target server or server group from the Upload files to list. Choose one of the existing configurations or create a new one: click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and [configure access to the relevant server](creating-in-place-server-configuration.html), or [set up a server group](server-groups.html) in the dialog that opens.

![Upload files from after commit area](https://resources.jetbrains.com/help/img/idea/2025.3/upload_files_from_after_commit_area.png)

To have your selection applied automatically in the future, select the Always use selected server or group of servers checkbox.

  3. Proceed with [committing your changes](commit-and-push-changes.html#commit).




### Configure automatic upload of changed files to the default server or server group

IntelliJ IDEA considers a local file changed as soon as it is saved either automatically or manually (File | Save All or `Ctrl+S`), see [Save and revert changes](saving-and-reverting-changes.html). Changed files can be automatically uploaded only to the [default deployment server](configuring-synchronization-with-a-remote-host.html#default_server).

  1. Open the [Options](settings-deployment-options.html) dialog by doing one of the following:

     * Go to Tools | Deployment | Options.

     * In the Settings dialog (`Ctrl+Alt+S`) , go to Build, Execution, Deployment | Deployment | Options.

  2. From the Upload changed files automatically to the default server list, choose when you want IntelliJ IDEA to upload changed files:

     * To upload any manually or automatically saved file, choose Always.

     * To upload only manually saved files, choose On explicit save action.

     * To suppress automatic upload, choose Never.

  3. If you enabled automatic upload, optionally configure the scope it should apply to:

     * Select Skip external changes to exclude local changes that were made using a third-party tool (a VCS, a script, and so on) from automatic upload.

     * Select Delete remote files when local are deleted to have IntelliJ IDEA automatically delete remote files during automatic uploads in case the local ones are deleted.

Note that this option serves as an extra safety measure and may result in unwanted files remaining on the remote server. As an example, consider a local file FILE.md, which is renamed to RENAMED.md. Since renaming a file is technically indistinguishable from deleting the file and creating a new one, the following will happen after automatic upload:

       * If the option is enabled, the remote server will only contain RENAMED.md.

       * If the option is disabled, the remote server will contain both FILE.md and RENAMED.md after automatic upload. You will probably need to delete FILE.md manually afterwards.




Enabling the Upload changed files automatically to the default server option also enables [Upload to default server](saving-and-reverting-changes.html#actions-on-save) in Settings | Tools | Actions on Save.

### Download a file or folder

  1. In the main menu, go to Tools | Deployment | Browse Remote Host.

  2. In the Remote Host tool window that opens, select the required file or folder and choose Download from Here from the context menu of the selection.

![Download a file or folder](https://resources.jetbrains.com/help/img/idea/2025.3/download_from_here.png)



### Download a file from the default deployment server

  * In the main menu, go to Tools | Deployment | Download from <default server>.

IntelliJ IDEA will prompt you to overwrite local files, if any.




11 October 2024

[Access files on servers](accessing-files-on-remote-hosts.html)[Compare deployed files and folders with their local versions](comparing-deployed-files-and-folders-with-their-local-versions.html)
