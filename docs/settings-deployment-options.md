[//]: # (Source: https://www.jetbrains.com/help/idea/settings-deployment-options.html)
[//]: # (Downloaded: 2025-12-17 20:00:50)

# Options

Use this page to specify additional configuration settings for uploading and downloading project files to and from local and remote servers. For more information about various server access configurations, refer to [Deployment](deploying-applications.html). 

The options specified in this dialog apply to all defined server configurations regardless of the server type (local, remote) and the data transfer protocol used. Protocol-specific options for server configurations of the type FTP/SFTP/FTPS/WebDAV are defined on the [Connection tab](deployment-connection-tab.html) of the [Deployment](settings-deployment.html) page of the Settings dialog.

Item| Description  
---|---  
Exclude items by name| In this field, specify patterns for the names of files and folders that you do not need to be deployed. Use semicolons `;` as delimiters, asterisks `*` to match zero or more characters, and question marks `?` to match a single character.For example, if you have a folder stylesheets with three files style.css, style1.css, and style2.scss, then `style*` excludes the entire folder, `style?.css` excludes style1.css, and `style?.*` excludes style1.css and style2.scss.Learn more from [Regular-Expressions.info](https://www.regular-expressions.info/quickstart.html).The exclusion is applied recursively. This means that if a matching folder has subfolders, the contents of these subfolders are not deployed either.  
Operations logging| Use this list to specify how much detailed logging you need to have. The available options are:

  * Errors only: select this option to have the log show only errors occurred during upload.
  * Brief: select this option to have all events reflected in the log but without details.
  * Details: select this option to have more details on the upload shown in the log, for example, full file paths.

  
Overwrite up-to-date files| If this checkbox is selected, all files will be uploaded no matter whether they have been changed since the previous upload or not.Otherwise, if this checkbox is not selected, only the files that have been changed since the previous upload will be uploaded.  
Use a temporary file during upload| Select this checkbox to use a temporary name for the changed file that is being uploaded to the server, and only rename it back after the upload operation has been successfully completed.  
Preserve file timestamps| Select this checkbox to prevent resetting timestamps of files on upload.  
Delete target items when source ones do not exist (when transferring from Project view or Remote Host view)| If this checkbox is selected, any file in the destination directory will be removed if the file with this name is not involved in the current upload.This option is applicable when synchronization if performed from the [Project](project-tool-window.html) tool window or from the [Remote Host](remote-host-tool-window.html) tool window.  
Create empty directories| Select this checkbox to have an empty directory on the server created automatically if a new local directory has been created in your project since the last upload in the source folder.  
Prompt when overwriting or deleting local items| Select this checkbox to have IntelliJ IDEA prompt for confirmation before overwriting or deleting local items for synchronization during download.  
Confirm uploading files| Select this checkbox to have IntelliJ IDEA prompt for confirmation before uploading local items to a remote host.  
Upload changed files automatically to the default server| From this list, choose when you want IntelliJ IDEA to automatically upload a file to the default server or server group. The available options are:

  * Always: upload a file upon every automatic and explicit save. 
  * On explicit save action: upload a file after save only if this save was invoked manually by choosing File | Save All or pressing `Ctrl+S`.
  * Never: suppress automatic upload.

The default server configuration or a server group is appointed on the [Deployment](settings-deployment.html) page by selecting the desired item in the list and clicking the Use as Default toolbar button ![icon use web server configuration as default](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.setDefault.svg).  
Skip external changes| Select this checkbox to exclude local changes that were made using a third-party tool (a VCS, a script, and so on) from automatic upload.The checkbox is available only when the Always or On explicit save action option is selected in the Upload changed files automatically to the default server list.   
Delete remote files when local are deleted| Select this checkbox to have IntelliJ IDEA automatically delete remote files during automatic uploads in case the local ones are deleted. The checkbox is available only when the Always or On explicit save action option is selected in the Upload changed files automatically to the default server list. Note that this option serves as an extra safety measure and may result in unwanted files remaining on the remote server. As an example, consider a local file FILE.md, which is renamed to RENAMED.md. Since renaming a file is technically indistinguishable from deleting the file and creating a new one, the following will happen after automatic upload:

  * If the option is enabled, the remote server will only contain RENAMED.md.
  * If the option is disabled, the remote server will contain both FILE.md and RENAMED.md after automatic upload. You will probably need to delete FILE.md manually afterwards.

  
Preserve original file permissions| If enabled, IntelliJ IDEA will preserve the original local files' permissions when uploading files on remote hosts over FTP/FTPS.The option is only available for macOS and Linux.  
Override default permissions on files| Select this checkbox to change the default permissions assigned to uploaded files on remote hosts. Click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) to open the [Files Default Permissions](default-permissions.html) dialog, where you can manage access to uploaded files on remote hosts by assigning permissions.  
Override default permissions on folders| Select this checkbox to change the default permissions assigned to uploaded folders on remote hosts. Click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) to open the [Folders Default Permissions](default-permissions.html) dialog, where you can manage access to uploaded folders on remote hosts by assigning permissions.  
Warn when uploading over newer file| Use this list to define the version-control policy to apply when uploading files to remote hosts. Depending on this choice, IntelliJ IDEA either checks whether any changes have been made to the corresponding files on the remote host since you downloaded them or just overwrites the remote files.

  * No choose this option to have the file on the remote host overwritten with its local copy silently. All the changes made to the remote file since your last synchronization will be abandoned.
  * Compare timestamp & size if you choose this option, IntelliJ IDEA performs two checks:
    1. Compares the sizes of the local and remote files.
    2. Compares the remote file timestamp set at the moment of the last synchronization with the current remote file timestamp.
If the files differ in their size or the remote file timestamps differ, IntelliJ IDEA opens a [Diff Viewer for Files](differences-viewer.html), where you can explore and integrate the differences.This type of check depends on the timezone setting. If the timezone setting on your local machine is different from that on the remote host, the check may be successful even though the file versions actually differ.
  * Compare content when this option is chosen, IntelliJ IDEA compares the content of the local and remote files. If any diversions are detected, IntelliJ IDEA opens a [Diff Viewer for Files](differences-viewer.html), where you can explore and integrate the differences.

  
Notify of remote changes| Select this checkbox to receive notifications about changes on the remote host. The checkbox is available only when the Compare timestamp and size or Compare content option is selected in the Warn when uploading over newer file list.  
  
11 October 2024

[Deployment: Excluded Paths Tab](deployment-excluded-paths-tab.html)[Files/Folders Default Permissions dialog](default-permissions.html)
