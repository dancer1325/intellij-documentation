[//]: # (Source: https://www.jetbrains.com/help/idea/version-control-tool-window-update-info-tab.html)
[//]: # (Downloaded: 2025-12-17 20:06:10)

## Toolbar

Item| Tooltip and Shortcut| Description  
---|---|---  
Filter| N/A| Use this field to search through the list of commits. You can enter full commit names or messages or their fragments, revision numbers, or regular expressions.  To finalize the search, press `Enter` or move the focus away from the search field. You can quickly switch the focus to the search field by pressing `Ctrl+L`.  
![Find](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.toolwindow.find.svg)| N/A| Click to display previous search patterns.  
![the Clear icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.closeSmall.svg)| N/A| Click to clear the search and return to the full list of commits.  
![the Gear icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg)| Text Filter Settings| Click to select from the following options: 

  * Regex: anything you type in the search field is treated as a [regular expression](regular-expressions.html), for example, `#\d+`.
  * Match Case: only entries with the matching case count.

  
Branch| N/A| Use this drop-down to filter commits by branch or [favorite branches](manage-branches.html#favorite_branches). If you want to see commits from all local and remote branches, select All.  
User| N/A| Use this list to filter commits by author. To view all commits by a specific author, click Select and start typing the author's name. To view commits by all users, select All.  
Date| N/A| Use this list commits by a time-frame or a specific date. To view commits made on a specific date, click Select and specify the date. To view commits made on all dates, select All.  
Paths| N/A| Use this list commits by the folder (for projects that have one root), or by the root and folder (for multi-rooted projects). To view commits to a specific folder, click Select Folders and specify the folder name. For multi-repository projects, you can also select the checkbox next to one or several roots in the Roots section.  
![the Refresh icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.refresh.svg)| Refresh`Ctrl+F5`| Click this button to refresh the list of commits.  
![the Cherry-Pick button](https://resources.jetbrains.com/help/img/idea/2025.3/app.icons.cherryPick.svg)| Cherry-pick| Click to [apply changes from the selected commit to the current branch](apply-changes-from-one-branch-to-another.html#cherry-pick). This button is disabled if the selected commit is already contained in the current branch.  
![the IntelliSort button](https://resources.jetbrains.com/help/img/idea/2025.3/app.icons.IntelliSort.svg)| IntelliSort| If this option is enabled, you get a more convenient way to view merges by displaying incoming commits first, directly below the merge commit.  
![the Eye icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.show.svg)| Presentation Settings| Click to invoke the list of options that let you configure how data is presented in the Log tab of the Version Control tool window `Alt+9`

  * Compact References View: if this option is enabled, branch references for a single commit are displayed in a collapsed view: ![Compact references view](https://resources.jetbrains.com/help/img/idea/2025.3/compactReferenceView.png)If you want to expand each branch reference on a line, deselect this option: ![Expanded references view](https://resources.jetbrains.com/help/img/idea/2025.3/expandedReferencesView.png)
  * Show Tag Names: enable this option if you want tag names to be displayed in addition to the tag icon: ![the tag name](https://resources.jetbrains.com/help/img/idea/2025.3/showTagName.png)If this option is disabled, you can still view a tag name by hovering over the tag icon.
  * Show Long Edges: if this option is enabled, long branches are displayed in full, even if there are no commits in them. If this option is disabled (by default), long branches are replaced with a down arrow.
  * Collapse Linear Branches: enable this option to collapse all branches on the graph so that a dotted line is shown instead of successive commits.It is also possible to collapse an individual expanded branch by clicking it.
  * Expand Linear Branches: enable this option to expand all collapsed branches to show successive commits on the graph.It is also possible to expand an individual collapsed branch by clicking it.
  * Highlight: select if you want to highlight the following: 
    * My Commits: bold font
    * Merge Commits: greyed out
    * Current Branch: blue background
    * Non-Picked Commits: greyed out (only available for Git). Non-picked commits are commits from the selected branch that have not yet been applied to the current branch.

  
Show columns| Select which columns you want to see: author, date, and hash.  
![the Open Another Log Tab icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.openNewTab.svg)| Open Another Log Tab| Click to open a new log tab matching your filters, so that you don't have to set filters back and forth.  
![the Search icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.toolwindow.find.svg)| Go to Hash/Branch/Tag`Ctrl+F`| Click this button and specify a hash, tag or branch you want to jump to. ![Search by hash or branch/tag name](https://resources.jetbrains.com/help/img/idea/2025.3/vcs_find_hash_branch_tag_action.png) You can select a reference with the same name from different repositories. The name of each repository is displayed on the right along with its color indicator.  
  
Select Favorites to view commits in all branches [marked as favorites](manage-branches.html#favorite_branches).
