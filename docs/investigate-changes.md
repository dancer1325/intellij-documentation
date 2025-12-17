[//]: # (Source: https://www.jetbrains.com/help/idea/investigate-changes.html)
[//]: # (Downloaded: 2025-12-17 19:30:06)

## Review project history

You can review all changes made to a project sources that match the specified filters. To view project history, open the Log tab of the Git tool window `Alt+9`. It shows all changes committed to all branches and remote repositories:

![log view](https://resources.jetbrains.com/help/img/idea/2025.3/git_log_view.png)

In multi-repository projects, the colored stripe on the left indicates which root the selected commit belongs to (each root is marked with its own color). Hover over the colored stripe to invoke a tip that shows the root path: 

![root path](https://resources.jetbrains.com/help/img/idea/2025.3/log_root_path.png)

### Navigate and search through project history

  * Search through the list of commits by entering full commit names or messages or their fragments, revision numbers, or regular expressions.

  * Filter the commits by branch or favorite branches, user, date, and folder (or root and folder for multi-root projects).

  * Click the Go to Hash/Branch/Tag ![go to](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.toolwindow.find.svg) icon on the toolbar or press `Ctrl+F` and specify a commit hash, [tag](use-tags-to-mark-specific-commits.html) or the name of a branch you want to jump to (you will be taken to the latest commit in that branch).

  * Click an arrow to jump to the next commit in a long branch: 

![jump to next commit](https://resources.jetbrains.com/help/img/idea/2025.3/jumpToNextCommit.png)
  * Press the `Left` and `Right` keys to jump to the parent/child commit. This is especially useful if you have commits to different repositories and multiple branches all mixed in the Log tab of the Git tool window `Alt+9`.




  * Switch the focus to the search field by pressing `Ctrl+L`.

  * To avoid setting filters back and forth, click ![add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) on the toolbar to open a new tab matching your filters.

  * To customize the date format, go to Settings | Appearance and Behavior | System Settings | Date Formats.




For more information about the Log tab of the Git tool window `Alt+9`, refer to [Log tab](log-tab.html).
