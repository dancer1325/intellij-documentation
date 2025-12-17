[//]: # (Source: https://www.jetbrains.com/help/idea/non-project-files-access-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:33:18)

# Non-project files protection

This dialog appears when you try to edit non-project files: library sources, external sources and so on. Such files are intentionally protected from modification. For example, it is not recommended that you change library classes as you are supposed to reuse them as is. 

If you want to work with these files, add them to the content root. A content root in IntelliJ IDEA is a folder that contains your source code, build scripts, unit tests, and documentation. In the Project tool window, this folder is marked with the ![Directory](https://resources.jetbrains.com/help/img/idea/2025.3/app.nodes.folder.svg) icon. For more information about content roots, refer to [Content roots](content-roots.html). To move a file or a folder to another location, you can use the [Move](move-refactorings.html#move_refactoring) refactoring. 

If you want to edit these files only once without adding them to your project, use one of the options in the dialog.

![Non-Project Files Protection dialog](https://resources.jetbrains.com/help/img/idea/2025.3/non-project-files-access.png)

  * This file: select this option to disable protection for the file or files.

  * All files in this directory: select this option to disable protection for the listed files and all files in the same directory.

  * Any non-project file: select this option to disable protection.




All options are effective during the current session. Once the IDE is restarted, protection will be re-enabled. Also, you cannot change your decision for a particular file within the current session.

03 September 2025

[File type associations](creating-and-registering-file-types.html)[Resource files](resource-files.html)
