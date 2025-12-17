[//]: # (Source: https://www.jetbrains.com/help/idea/version-control-tool-window-history-tab.html)
[//]: # (Downloaded: 2025-12-17 20:06:06)

# History tab

The History tab is added to the Version Control tool window `Alt+9` on invoking the Show History or Show History for Selection action. A new tab is created for each file or directory with the following name: History: <file_name>. The set of toolbar buttons differs slightly depending on your version control system.

The asterisk next to a commit marks commits where the author and the user who committed the changes are different.

Item| Tooltip and Shortcut| Description  
---|---|---  
Branch| Branch filter| Click Branch and select a branch to review changes made to a file within this branch.  
![the Refresh button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.refresh.svg)| Refresh| Click this button to refresh the current information.  
![the Show diff icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.vcs.diff.svg)| Show Diff`Ctrl+D`| Click this button to compare the selected revision of a file with its previous revision in the [Diff Viewer](differences-viewer.html).  
![the Show All Affected Files button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.vcs.changes.svg)| Show All Affected Files`Alt+Shift+A`| Click this button to open the Paths Affected in Revision dialog, where you can view all files that were modified in the selected revision.  
![the Eye icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.show.svg)| View Options| Click to choose the amount of information you want to see in the History view. You can also select the Show Commit Timestamp option if you want IntelliJ IDEA to show the commit timestamp instead of the time when a change was authored.Also, select the type of info you want to see:

  * Show Details to display the commit message for the selected revision.
  * Show Diff Preview to open a diff preview for the selected revision.

  
![the Open on GitHub button](https://resources.jetbrains.com/help/img/idea/2025.3/app.vcs.vendors.github.svg)| Open on GitHub| Click this button to open the page that corresponds to the selected commit on [GitHub](https://github.com/).  
![](https://resources.jetbrains.com/help/img/idea/2025.3/vcs-gitlab.org.jetbrains.plugins.gitlab.gitLabLogo.svg)| Open on GitLab| Click this button to open the page that corresponds to the selected commit on [GitLab](https://about.gitlab.com/).  
![the Resume button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.progress.resume.svg)| Enable Git Log Indexing| Click this button to improve working with the history of changes across the IDE. Indexing project repositories allows:

  * Fast log filtering and computing precise history.
  * Displaying all branches in file history.
  * Searching across history in Search Everywhere.

To disable this option, go to Settings | Version Control | Confirmation | Log.  
![Renaming](https://resources.jetbrains.com/help/img/idea/2025.3/renaming.png)| Renaming column| Click this column to expand it and review the history of the file's renaming. Hover over the column to see the changes in the file's path.  
  
26 August 2024

[Log tab](log-tab.html)[Integrate to branch info view](version-control-tool-window-integrate-to-branch-info-view.html)
