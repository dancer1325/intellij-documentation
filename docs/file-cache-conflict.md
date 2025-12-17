[//]: # (Source: https://www.jetbrains.com/help/idea/file-cache-conflict.html)
[//]: # (Downloaded: 2025-12-17 19:26:49)

# File cache conflict

If an external process changes a file that was opened and unsaved in IntelliJ IDEA, it results in two conflicting versions of the file.

Prevent other applications from modifying the files that are already opened in the IDE or use the following options to resolve conflicts.

Item| Description  
---|---  
Load FS Changes| Click this button to load the file version produced outside of IntelliJ IDEA, and overwrite your local changes.  
Keep Memory Changes| Click this button to preserve the version produced in IntelliJ IDEA and stored in cache.  
Show Difference| Click this button to invoke the [Diff Viewer](differences-viewer.html) that shows the version in the file system to the left, and IntelliJ IDEA version to the right. You can merge differences as required and load the desired version to IntelliJ IDEA. By default, the cache version is saved.  
  
29 August 2025

[Create run/debug configuration for Gradle tasks](create-run-debug-configuration-gradle-tasks.html)[Find Usages](find-usages-dialog.html)
