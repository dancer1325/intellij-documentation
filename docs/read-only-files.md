[//]: # (Source: https://www.jetbrains.com/help/idea/read-only-files.html)
[//]: # (Downloaded: 2025-12-17 19:56:46)

# Read-only files

If a file is read-only, it is marked with the closed lock icon ![the Locked icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.locked.svg) in the [status bar](guided-tour-around-the-user-interface.html#read_only_widget). If a file is writable, it is marked with the open lock icon ![the Unlocked icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.unlocked.svg).

### Toggle read-only mode on and off

  * Open a file in the editor and click the lock icon ![the Locked icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.locked.svg)/![the Unlocked icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.unlocked.svg) in the [status bar](guided-tour-around-the-user-interface.html#status-bar).

  * Alternatively, select a file in the Project tool window (`Alt+1`), go to File | File Properties in the main menu and click Make file read-only. 

![Making file read-only](https://resources.jetbrains.com/help/img/idea/2025.3/file_readonly.png)



Files can be read-only in certain cases. In these cases, clicking the ![the Locked icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.locked.svg)/![the Unlocked icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.unlocked.svg) icon the status bar will not make the file writable.

  * The file is a [decompiled class](decompiler.html). Complied classes are normally read-only in IntelliJ IDEA.

  * The read-only status is set by a version control system. For example, the file can be [locked](locking-and-unlocking-files-and-folders.html) by Subversion.

In this case, use IntelliJ IDEA version control integration features to make the file writable.

  * The file size exceeds 2.5 MB. Such files are considered too large for editing.

  * Library files in IntelliJ IDEA are normally read-only by default as the code from them should be used as is. For such files, you will not see the lock icon in the status bar. IntelliJ IDEA applies [Reader mode](reader-mode.html) to library files by default.

  * The file does not belong to the project. In this case, the [Non-Project Files Protection](non-project-files-access-dialog.html) dialog appears, prompting you to select an action.

  * The file belongs to the generated sources ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.nodes.generatedSource.svg) or generated test sources ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.nodes.generatedTestRoot.svg) root. Files in these folders are usually read-only as they are generated automatically rather than written manually and can be regenerated. Learn more about different types of folders from [Content roots](content-roots.html). 

  * The file may be marked as read-only in your operating system. To check this status, you can inspect file attributes on Windows or permissions on Unix-based systems like Linux or macOS.




15 July 2025

[Share file templates](share-file-templates.html)[Compare files, folders, and text sources](comparing-files-and-folders.html)
