[//]: # (Source: https://www.jetbrains.com/help/idea/big-data-tools-data-files.html)
[//]: # (Downloaded: 2025-12-17 19:18:57)

# Work with data files

Once you have established a connection to a remote storage, you can work with the data files. With the [Remote File Systems](https://plugins.jetbrains.com/plugin/21706-remote-file-systems) plugin, you can manage buckets, perform basic file operations, quickly find a file and navigate to it, and more.

You can also preview large structured files (Parquet, ORC, Avro, and CSV) in tabular form. This functionality is provided by the [Big Data File Viewer](https://plugins.jetbrains.com/plugin/21701-big-data-file-viewer), which is installed automatically with the Remote File Systems plugin.

### Manage server directories

  1. Expand the server node to preview its structure.

  2. Right-click a directory to open the context menu.

![Context menu in the Big Data Tools tool window](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_directories_menu.png)

You can copy, paste, rename the directory, change its location, copy its path, and add new files and directories. Select Upload from disk to add more files to the directory. You can also save the directory and its files on the local drive.

  3. To quickly create a new bucket, file, directory, or connection, press `Alt+Insert`. 

![Create New](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_storage_intention_actions.png)



### Navigate to a file

The Big Data Tools tool window lets you quickly locate files and directories in your storage. It can be useful if you have a lot of nested directories and do not want to click and expand each of them when looking for a file. Instead, you can start typing a path to it and let IntelliJ IDEA show your available files and autocomplete the path.

  1. Select a connection to a storage and click ![Find icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.toolwindow.find.svg) at the top of the Big Data Tools tool window or press `Ctrl+F`. You can select a particular bucket or directory if you want to find a file within it.

  2. In the Navigate in window, start typing a path to the file or directory. Press `Tab` to autocomplete the path. Or you can type the name of a bucket to quickly find it. 

![Navigate in window](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_navigate_in_storage.png)
  3. Press `Enter`.




This will locate the selected file in the Big Data Tools tool window.

If your file is opened in the editor, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.locate.svg) (Select Opened Files) in the Big Data Tools tool window to locate this file in a Remote File System connection.

### Manage data files

  1. Expand the target directory and select a file.

  2. Right-click the file to open the context menu. 

![Context menu to work with the data files](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_manage_files.png)
  3. You can copy, paste, rename the file, copy its path, change its location, or delete it.

  4. To briefly preview details of a structured file, such as CSV, Parquet, ORC, or Avro, expand it in the editor or in the Big Data Tools tool window. You should be able to see the columns and their types.

![Expanded data file](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_expand_csv.png)

Select Show Info from the context menu to obtain more details about the file:

![File info](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_file_info.png)
  5. To view a file, double-click it or select the Preview command from the context menu. The file opens in the editor. You cannot [edit it](#edit_files) but you can preview it as a table or as text:

![Table view of the csv file](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_table_view_csv.png)

![Text view of the csv file](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_text_view_csv.png)

In the table view, you can operate with table elements. Right-click to open the context menu and select a command to copy a raw or a column, or copy the entire table to the clipboard or file.

![Table-specific commands](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_table_context_menu.png)

You can also sort data in columns by clicking column headers.

When you open .parquet files, the plugin only displays the first portion of the file content. This is especially useful when you work with very large files.




### View files in the editor

  1. To open any storage or directory in a separate tab of your editor, select the item in the Big Data Tools tool window and click ![Open in Editor button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.export.svg).

![Open a directory in editor](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_open_dir_file_viewer.png)
  2. The selected directory will be opened in a separate tab of the editor. 

![Preview a directory](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_file_viewer.png)

You can exchange files with the servers and directories opened in the Big Data Tools tool window. Use the viewer toolbar icons to copy, paste, and cut files.

  3. You can customize the visual appearance of the storage:

     * Click ![File info](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.previewDetails.svg) to manage visibility of the file info details.

     * Click ![Show and hide columns icon](https://resources.jetbrains.com/help/img/idea/2025.3/bigdatatools-core.icons.table.configureColumns.svg) to exclude any column for a view. By default, all columns are displayed in the viewer.

  4. Click ![Refresh](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.refresh.svg) to update the content of the selected directory.




Use the ![More actions](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.more.svg) to get access to other commands.

### Drag and drop files

With IntelliJ IDEA, you can easily copy and move files between different remote file systems or within the same storage by dragging them to needed buckets, containers, or directories. You can also quickly upload a file from your local file system to a remote one by dragging the file from your Project tool window to the editor, which can be opened in the editor or in the Big Data Tools tool window.

  1. Drag a file to the necessary bucket, container, or directory

  2. In the window that opens, confirm the name of the file and destination directory.

![Dragging a file to storage](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_drag_and_drop.png)



When you drag a file within the same connection, IntelliJ IDEA removes the file from the original location. When you drag a file from your project or from one connection to another one, IntelliJ IDEA creates a copy of the file.

### Edit files

Once you have established connection to a remote storage, you can edit text files in this storage except for Zeppelin notebooks and delimiter-separated files, such as CSV.

  1. Double-click a file to open it in the editor.

  2. Modify the file. At the top of the files, icons become available allowing you to:

     * Show the diff (![the Diff icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.vcs.diff.svg))

     * Revert the file content to its initial state, as it was when you opened it (![the Revert icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.rollback.svg))

     * Retrieve the latest file changes from the server (![the Reload icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.refresh.svg))

     * Submit your file changes to the server (![the Save icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.save.svg))

![Editing a remote file](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_change_remote_file.png)



### View file versions

Versioning lets you have multiple variants of the same object in a storage. If versioning is enabled for a bucket, you can view versions of the objects right in IntelliJ IDEA. You can also upload, download, delete, restore, and compare specific versions.

To view and manage file versions, versioning must be enabled in the corresponding bucket. For more information, refer to your storage documentation (for example, [Enabling versioning on buckets](https://docs.aws.amazon.com/AmazonS3/latest/userguide/manage-versioning-examples.html) for AWS S3 buckets).

  1. In the Big Data Tools tool window, select a storage and click ![Open in Editor button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.export.svg) to open it in the editor.

  2. Expand a bucket, for which versioning is enabled, and select a file in the bucket.

  3. In the Details pane, open the Versions tab.




The tab displays all available versions of the selected file.

![Versions tab](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_tencent_versions_tab.png)

When you select a version, the following icons become available:

  * ![Upload](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.upload.svg) upload a new version of the file from your local drive.

  * ![Download](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.download.svg) download the selected version of the file.

  * ![Delete](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.gc.svg) delete the selected version of the file.

  * ![Restore](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.restart.svg) restore the selected version of the file.

  * ![Show Diff](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.vcs.diff.svg) show the diff between the selected and the previous versions of the file (or you can select two versions if you want to show the diff between them).




### Create a new bucket

  1. To add a new bucket to the data storage, right-click the storage connection in the Big Data Tools tool window and select Create Bucket from the context menu. 

  2. Specify the new bucket name and click Ok to complete the task.




### Filter the list of buckets

If you want to work with part of your storage rather than the whole storage, you can filter buckets (or containers in terms of Microsoft Azure) that you want to be displayed in the Big Data Tools tool window and in the [editor](#file-viewer).

You can either specify custom paths to buckets and directories or filter buckets by name. You can do it when configuring a new connection, or you can tweak earlier configured connection settings.

  1. In the Big Data Tools tool window, select a server and click ![connection settings](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) on the window toolbar.

  2. Choose the way to filter buckets:

     * Select Custom roots and, in the Roots field, specify the name of the bucket or the path to a directory in the bucket. You can specify multiple names or paths by separating them with a comma.

     * Select All buckets in the account (or All containers in the account for Azure). You can then use the bucket filter to show only buckets with particular names.

     * For AWS S3 connections, you can also select Only buckets from in the selected region to get bucket from a specific region. For other storages, buckets are always filtered based on the region selected for connection.

![Filtering the list of buckets](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_filter_buckets.png)



In case the server connection has been lost, the corresponding icon shows the disconnected status of the server ![Server connections got lost](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.error.svg).

![Disconnected server](https://resources.jetbrains.com/help/img/idea/2025.3/bdt_troubleshoot_connections.png)

Click ![Refresh connections](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg) to reestablish the connection to the server.

06 June 2025

[Local file system](big-data-tools-local-file-system.html)[Amazon EMR](big-data-tools-aws-emr.html)
