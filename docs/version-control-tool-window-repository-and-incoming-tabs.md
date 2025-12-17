[//]: # (Source: https://www.jetbrains.com/help/idea/version-control-tool-window-repository-and-incoming-tabs.html)
[//]: # (Downloaded: 2025-12-17 20:06:09)

## Changelists Pane

The pane shows the changelists committed and stored in the history cache. When you click a changelist, the files affected by the selected commit are displayed in the [Changed Files](#right) pane.

Committed changelists often correspond to issues in tracking systems. You can have such issues opened in the browser right from the Changelists pane. This functionality has the following prerequisites:

  * The [pattern](handling-issues.html#issueNavigationPattern) of the bug tracking system is specified in the [Issue Navigation](handling-issues.html) Settings Preferences dialog.

  * The corresponding issue number is mentioned in the commit message.




After issue navigation has been configured, issue numbers in commit messages are rendered as links. Clicking such link brings you to the corresponding page of your issue tracker.

Item| Tooltip and Shortcut| Description| Available In  
---|---|---|---  
![Refresh](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.refresh.svg)| Refresh`Ctrl+F5`| Click this button to refresh the information in the view.| Both tabs  
![View details](https://resources.jetbrains.com/help/img/idea/2025.3/icon_viewDetails.png)| Show Details`Ctrl+Q`| Click this button to show the following information on the selected changelist: 

  * Changelist number
  * User and client name
  * Date and time of commit

| Both tabs  
![Patch](https://resources.jetbrains.com/help/img/idea/2025.3/app.vcs.patch.svg)| Create Patch| Click this button to [create a patch](using-patches.html) based on the selected changelist.| Repository tab  
![Rollback](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.rollback.svg)| Revert Changes| Click this button to create a _reverse patch_ for the selected changelist and roll back the changes made previously. You can use this action to revert changes committed by any user. The Select Target Changelist dialog opens.Note that if the reverse patch applies to a version committed earlier, this rollback attempt may fail because of the conflicts with the later changes.| Repository tab  
![the Clear button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.gc.svg)| Clear| Click this button to clear the history cache. The list of commits will be emptied. To restore it, click [Refresh](#refresh).| Repository  
![Edit](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg)| Edit Revision Comment| Click this button to edit the message for the selected commit.| Repository  
![Check out](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.checkOut.svg)| Update Project`Ctrl+T`| Click this button to update the project to the latest available version.| Incoming tab  
![Expand all](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.expandAll.svg)| Expand All`Ctrl+NumPad +`| Click this button to expand all nodes.| Both tabs  
![Collapse all](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.collapseAll.svg)| Collapse All`Ctrl+NumPad -`| Click this button to collapse all nodes.| Both tabs  
![Copy](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.copy.svg)| Copy`Ctrl+C`| Click this button to copy the commit message of the selected changelist to the Clipboard.| Both tabs  
![the Help icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.help.svg)| Help `F1`| Open a browser and show the corresponding help page.| Both tabs  
![Highlight integrated](https://resources.jetbrains.com/help/img/idea/2025.3/highlightIntegrated.png)| Highlight Integrated| Click this button to have the Merge Info pane displayed. The button is enabled only when both the server side and the client side use Subversion 1.5.| Repository tab  
Filter by| Use this list to hide the changelists that are of no interest to you, and view only the changelists that satisfy a certain criterion. The following options are available:

  * User: select this option to filter the commits by the user.
  * Structure: select this option to filter the commits by the target module or folder.
  * Client: select this option to filter the commits by the computer from which they were made.
  * None: select this option to turn off filtering and return to the default view.

| Both tabs  
Group by| Use this list to group changelists following a certain criterion. The following options are available:

  * Date: select this option to group the commits by date.
  * User: select this option to group the commits by users.
  * Client: select this option to group the commits by the computer from which they were made.

| Both tabs  
Search| Use this field to enter a search pattern and locate the commits whose commit messages matches the specified string. As you type, the list dynamically reduces to show the changelists with the commit messages that match the specified pattern. To save the search pattern, press `Enter`.To view the list of recent search patterns, click the ![Find](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.toolwindow.find.svg) button.To clear the list of search patterns, click the ![Clear](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.closeSmall.svg) button.| Repository tab
