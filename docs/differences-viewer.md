[//]: # (Source: https://www.jetbrains.com/help/idea/differences-viewer.html)
[//]: # (Downloaded: 2025-12-17 19:25:00)

## Diff & Merge viewer

Item| Tooltip and Shortcut| Description  
---|---|---  
![the Previous Difference button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.up.svg)/![the Next Difference button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.down.svg)| Previous Difference / Next Difference `Shift+F7` `F7`| Jump to the next or previous difference.When the last or the first difference is reached, IntelliJ IDEA suggests clicking the arrow buttons or pressing `F7`/`Shift+F7` once more and comparing other files modified locally. This behavior depends on the [Go to the next file after reaching last change](settings-tools-diff-and-merge.html#last_diff) option in the [Diff Viewer settings](settings-tools-diff-and-merge.html).  
![the Compare Previous File icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.left.svg)![the Compare Next File icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.right.svg)| Compare Previous/Next File `Alt+Left``Alt+Right`| Compare the local copy of the previous or next file with its update from the server.These controls are only available if more than one file has been modified locally.  
![the Go To Changed File icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.listFiles.svg)| Go To Changed File `Ctrl+N`| Display all changed files in the current change set and navigate to them. This action is only available when you review changes to multiple files.  
![the Jump to Source button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.edit.svg)| Jump to Source `F4`| Open the selected file in the editor. The caret is placed in the same position as in the Diff Viewer.  
Viewers| Select a viewer mode: side-by-side or unified. The side-by-side mode has two panels, and the unified mode has one panel.You can edit code and perform the Accept, Append, Revert actions in both viewers.You can change text only in the right part of the side-by-side viewer or in the lower line in the unified viewer.You can edit only local versions of your files. You cannot edit files that have read-only status.  
Whitespace| Define how the Diff Viewer should treat whitespaces.

  * Do not ignore: white spaces are important, and all the differences are highlighted. This option is selected by default.
  * Trim whitespaces: trim whitespaces if they appear in the end and at the beginning of a line (`("\t", " ")`).
    * If two lines differ in trailing whitespaces only, these lines are considered equal.
    * If two lines are different, trailing whitespaces are not highlighted in the [By word](#highlight) mode.
  * Ignore whitespaces: white spaces are not important, regardless of their location in the source code.
  * Ignore whitespaces and empty lines: ignores whitespaces and empty lines. The following entities are ignored:
    * all whitespaces (as in the 'Ignore whitespaces' option)
    * all added or removed lines consisting of whitespaces only
    * all changes that consist of splitting or joining lines without changes to non-whitespace parts.For example, differences between `a b c` and `a \n b c` are not highlighted in this mode.
  * Ignore imports and formatting: changes within import statements and whitespaces are ignored (whitespaces within String literals are respected though).

  
Highlighting mode| Select the way differences granularity is highlighted.The available options are:

  * Highlight words: modified words are highlighted
  * Highlight lines: modified lines are highlighted
  * Highlight split changes: if this option is selected, big changes are split into smaller changes.For example, `A \n B` and `A X \n B X` are treated as two changes instead of one.
  * Highlight characters: modified symbols are highlighted
  * Do not highlight: if this option is selected, the differences are not highlighted at all.Use the Do not highlight option when you work with the files that were significantly modified. In such cases, highlighting might introduce additional difficulties during a review.

  
![the Collapse Unchanged Fragments icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.collapseAll.svg)| Collapse Unchanged Fragments| Collapse all the unchanged fragments in both files. The number of non-collapsible unchanged lines is configurable on the Diff & Merge settings page. To open the Diff & Merge page, open settings by pressing `Ctrl+Alt+S` and navigate to Tools | Diff & Merge. .  
![the Synchronize button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.actions.synchronizeScrolling.svg)| Synchronize Scrolling| Click this button to scroll both diff panes simultaneously. If this button is released, each of the panes can be scrolled independently.  
![the Settings button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.settings.svg)| Settings| Open a list of available settings.These commands are also available from the context menu of the Diff Viewer gutter.  
![the Swap Sides button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.swapPanels.svg)| Swap Sides| Click this button to swap the sides in the Diff Viewer. This action is available when you are comparing two files, a file with the Clipboard contents, or when you open a blank Diff Viewer and paste the contents you want to compare. For more information, refer to [Compare files, folders, and text sources](comparing-files-and-folders.html).   
| Include into commit `Alt+I`| This checkbox only appears if you invoke the Diff Viewer from the Commit Changes dialog with multiple changed files (all of which are deselected), and you explore the differences between them and hit the last difference in a file.Select this checkbox if you want to include the file you've reviewed in the commit.  
![the Help icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.help.svg)| Help `F1`| Open a browser and show the corresponding help page.  
| `Ctrl+Shift+Tab`| Switch between the panes of the Diff Viewer. The active pane has the caret.  
![apply left](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.diff.arrowRight%4014x14.svg) ![apply right](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.diff.arrow%4014x14.svg)| Accept| Apply differences between panes (in case of the side-by-side viewer) or between lines (in case of the unified viewer).The chevron buttons can change their behavior:

  * Click ![apply left](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.diff.arrowRight%4014x14.svg) and ![apply right](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.diff.arrow%4014x14.svg) to apply changes. This behavior is the default one.
  * Press `Ctrl` to change ![apply left](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.diff.arrowRight%4014x14.svg) or ![apply right](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.diff.arrow%4014x14.svg) to ![chevron button bottom right](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.diff.arrowRightDown%4014x14.svg) or ![chevron button bottom left](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.diff.arrowLeftDown%4014x14.svg) and append changes.

  
Merge actions  
![the Compare Contents icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.vcs.diff.svg)| Compare Contents| Click this icon to invoke the list of options allowing you to compare different versions of a file to resolve a conflict.Note that Base refers to the file version that the local and the repository versions originated from (initially displayed in the middle pane), while Middle refers to the resulting version.  
![the Apply Non-Conflicting Changes button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.diff.applyNotConflicts.svg)| Apply All Non-Conflicting Changes| Click this button to apply all non-conflicting changes. You can also make this behavior automatic by selecting the checkbox Automatically apply non-conflicting changes in the Diff & Merge page of the Settings dialog.  
![Apply Non-Conflicting Changes from the Left Side](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.diff.applyNotConflictsLeft.svg) ![Apply Non-Conflicting Changes from the Right Side](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.diff.applyNotConflictsRight.svg)| Apply Non-Conflicting Changes from the Left/Right Side| Click these buttons to merge non-conflicting changes from the left/right parts of the dialog.  
![the Resolve Simple Conflicts icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.diff.magicResolveToolbar.svg)| Resolve Simple Conflicts| Click this button to resolve simple conflicts (for example, if the beginning and the end of the same line have been modified in different file revisions) and merging the changes.Such conflicts are not resolved with the Apply non-conflicting changes actions since you have to make sure that they are resolved properly.  
| Annotate with GitBlame| This option is only available from the context menu of the gutter.Use this option to explore who introduced which changes to the repository version of the file and when. The annotations view lets you see detailed information for each line of code, such as the version from which this line originated, the ID of the user who committed this line, and the commit date.For more information about annotations, refer to [Locate code author (Annotate with Git Blame)](investigate-changes.html#annotate_blame).
