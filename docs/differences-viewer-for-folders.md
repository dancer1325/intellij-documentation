[//]: # (Source: https://www.jetbrains.com/help/idea/differences-viewer-for-folders.html)
[//]: # (Downloaded: 2025-12-17 19:24:58)

## Toolbar

Icon| Tooltip and shortcut| Description| Available for  
---|---|---|---  
![the Previous Difference button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.up.svg)/![the Next Difference button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.down.svg)| `F7` `Shift+F7`| Navigate between next and previous differences.When the last or first difference is hit, IntelliJ IDEA suggests to press `F7`/`Shift+F7` once more and compare other files.This feature becomes available only when the Diff Viewer is invoked from the Version Control tool window `Alt+9`.| Version control  
![the Jump to Source button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.edit.svg)| Jump to Source `F4`| Open a file in the active tab of the editor. The caret is placed in the same position as in the Diff Viewer.| All  
![Refresh](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.refresh.svg)| Refresh| Refresh the contents of the Diff Viewer.| All  
![Show new files on left side](https://resources.jetbrains.com/help/img/idea/2025.3/app.vcs.arrow_right.svg)| Show New Files on Left Side| Display items that are present in the first of the compared directories or database objects and are missing in the second one in the left pane.| All  
![Show diff in external tool](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.externalTools.svg)| Show diff in external tool| Invoke an external diff viewer. For more information about the external differences viewer, refer to the [External Diff Tools](settings-tools-external-diff-tools.html) page.This button is only available if the Use external diff tool option is selected in the [External Diff Tools](settings-tools-external-diff-tools.html) settings page.| All  
![Show difference](https://resources.jetbrains.com/help/img/idea/2025.3/app.vcs.not_equal.svg)| Show Difference| Display items that are present in both folders or database objects but have different contents, timestamp, or size.| All  
![Show equal files](https://resources.jetbrains.com/help/img/idea/2025.3/app.vcs.equal.svg)| Show Equal Files| Display items that are present in both directories or objects and have the same contents, timestamp, and size, depending on the parameter set in Compare by list.| All  
![Show new files on right sid](https://resources.jetbrains.com/help/img/idea/2025.3/app.vcs.arrow_left.svg)| Show New Files on Right Side| Show the items that are present in the second of the compared directories and are missing in the first one. The same rule applies to database objects.| All  
| Compare by| Applies the selected parameter for comparison. You can select between the following parameters:

  * Binary Content
  * Text (charset and line separators are ignored)
  * Size
  * Size and Timestamp

| Local foldersLocal-remote folders  
![Synchronize Selected](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.resume.svg)| Synchronize Selected `Enter`| Apply the [specified action](#suggested_action) to the selected pair of items.In the * column of the table, you can see actions that are going to be performed.| All  
![Synchronize All](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.run.rerun.svg)| Synchronize All `Ctrl+Enter`| Apply the [specified action](#suggested_action) to all the pairs of items in the list.In the * column of the table, you can see actions that are going to be performed.| All  
![the Swap Sides button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.swapPanels.svg)| Swap Sides| Click this button to swap the sides in the Diff Viewer.| All  
![Hide excluded files](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.filter.svg)| Hide excluded files| Hide files that are [excluded from synchronization](excluding-files-and-folders-from-deployment.html).| Local-remote folders  
| Filter| Filter objects in comparing folders.You can type a file or table name and filter all the objects according to this name. Use the asterisk wildcard (*) to replace any number of arbitrary characters.Note that filter applies when you press `Enter`.| All  
| Path| These fields show the paths to the folders that are compared. To change a directory, click the Browse button (![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg)) and specify another directory.| Local foldersLocal-remote folders  
![the Help icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.help.svg)| Help `F1`| Open a browser and show the corresponding help page.| All
