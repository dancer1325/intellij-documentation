[//]: # (Source: https://www.jetbrains.com/help/idea/comparing-deployed-files-and-folders-with-their-local-versions.html)
[//]: # (Downloaded: 2025-12-17 19:21:14)

## Comparing files and folders on the server with their local versions

Each remote file or folder is [mapped](creating-local-server-configuration.html) to one and only one local file or folder. Therefore, for each remote file or folder, IntelliJ IDEA detects its local version, so you can compare them at any time in the Diff Viewer.

The remote files in the Diff Viewer have the `read-only` status. This means that you cannot update them directly in the Diff Viewer. Make all the necessary changes to the local version of the file and upload the updated file to the server. 

### Compare a remote file with its local version

  1. Open the [Remote Host tool window](remote-host-tool-window.html) (Tools | Deployment | Browse Remote Host or View | Tool Windows | Remote Host) and select the required deployment server from the list. 

  2. Select the file, and then select Compare with local version from its context menu.

  3. In the [Diff Viewer for Files](differences-viewer.html) dialog that opens, explore the differences and apply them, if necessary, using the ![Replace from right](https://resources.jetbrains.com/help/img/idea/2025.3/app.diff.arrow.svg) button. For more information, refer to [Viewing Differences Between Files](comparing-files-and-folders.html#twofiles). 




### Compare a remote folder with its local version

  1. Open the [Remote Host tool window](remote-host-tool-window.html) (Tools | Deployment | Browse Remote Host or View | Tool Windows | Remote Host) and select the required deployment server from the list. 

  2. Select the folder and choose Sync with local from the context menu of the selection.

  3. In the [Diff Viewer for Folders](differences-viewer-for-folders.html) that opens, explore the differences and synchronize the files, where applicable. See [comparing two folders in the Diff Viewer](#compare_folders). 



