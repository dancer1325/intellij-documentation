[//]: # (Source: https://www.jetbrains.com/help/idea/resolving-property-conflicts-svn.html)
[//]: # (Downloaded: 2025-12-17 19:57:41)

# Resolve property conflicts

A property conflict is reported during synchronization with the server when IntelliJ IDEA detects differences between the properties of a local file or folder and their server version. IntelliJ IDEA does not attempt to resolve property conflicts automatically, and displays the conflicting files and folders under the Merged with property conflicts node in the [Update Info](version-control-tool-window-update-info-tab.html) tab of the Version Control tool window `Alt+9`. You have to resolve property conflicts manually and then tell IntelliJ IDEA to treat the corresponding files and folders as conflict-free.

### Resolve a property conflict

  1. Open the Version Control tool window `Alt+9` and switch to the [Repository](version-control-tool-window-repository-and-incoming-tabs.html) tab.

  2. In the [Changed Files](version-control-tool-window-repository-and-incoming-tabs.html#right) pane, select the conflicting file.

  3. Choose Properties Diff from the context menu of the selection, or click ![propertiesDiff.png](https://resources.jetbrains.com/help/img/idea/2025.3/propertiesDiff.png) on the toolbar.

  4. Explore the differences in the Subversion properties difference viewer: 

![svnPropertiesDiffRemoteResults.png](https://resources.jetbrains.com/help/img/idea/2025.3/svnPropertiesDiffRemoteResults.png)
  5. [Update the properties](working-with-subversion-properties-for-files-and-directories.html#create) so the conflict is resolved.




### To mark a file as resolved

  1. In the [Update Info](version-control-tool-window-update-info-tab.html) tab of the Version Control tool window `Alt+9`, select the fixed file under the Merged with property conflicts node. As you can see, the file is still displayed in red as conflicting.

  2. From the context menu of the selection, choose Subversion, and then choose Mark Resolved.

  3. When the dialog is closed, the Commit window shows the affected files as updated and available for checking in to the server.

  4. Check in the resolved files.




26 May 2024

[View differences in properties](viewing-differences-in-properties.html)[Diagnose problems with Subversion integration](diagnosing-problems-with-subversion-integration.html)
