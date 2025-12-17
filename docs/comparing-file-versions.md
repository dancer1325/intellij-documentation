[//]: # (Source: https://www.jetbrains.com/help/idea/comparing-file-versions.html)
[//]: # (Downloaded: 2025-12-17 19:21:15)

## Compare local changes with the base revision

Apart from [navigating](adding-files-to-version-control.html#track_changes) through your local changes within a file in the editor, you can review these changes compared to the base revision of the file.

To preview the diff, select a modified file in the Commit tool window and double-click it or press `Ctrl+D`.

The left pane shows the affected code as it was in the base revision, and the right page shows the affected code after you've made changes locally.

![Diff preview in the editor](https://resources.jetbrains.com/help/img/idea/2025.3/ij_diff_in_editor.png)

Use the toolbar buttons and controls to navigate between changes and configure the appearance of the Change Details pane or the Diff Viewer:

Item| Tooltip and Shortcut| Description  
---|---|---  
![the Previous Difference button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.up.svg)/![the Next Difference button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.down.svg)| Previous Difference / Next Difference `Shift+F7` `F7`| Jump to the next or previous difference.When the last or the first difference is reached, IntelliJ IDEA suggests clicking the arrow buttons or pressing `F7`/`Shift+F7` once more and comparing other files modified locally. This behavior depends on the [Go to the next file after reaching last change](settings-tools-diff-and-merge.html#last_diff) option in the [Diff Viewer settings](settings-tools-diff-and-merge.html).  
![the Jump to Source button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.edit.svg)| Jump to Source `F4`| Open the selected file in the editor. The caret is placed in the same position as in the Diff Viewer.  
![the Compare Previous File icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.left.svg)![the Compare Next File icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.right.svg)| Compare Previous/Next File `Alt+Left``Alt+Right`| Compare the local copy of the previous or next file with its update from the server.These controls are only available if more than one file has been modified locally.  
![the Go To Changed File icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.listFiles.svg)| Go To Changed File `Ctrl+N`| Display all changed files in the current change set and navigate to them. This action is only available when you review changes to multiple files.  
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
![the External Tools icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.externalTools.svg)| Show diff in external tool| Invoke an external diff viewer specified on the [External Diff Tools](settings-tools-external-diff-tools.html) settings page.This button is available only on the toolbar when the Use external diff tool option is enabled on the [External Diff Tools](settings-tools-external-diff-tools.html) settings page.  
![the Help icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.help.svg)| Help `F1`| Open a browser and show the corresponding help page.  
| Annotate with GitBlame| This option is only available from the context menu of the gutter.Use this option to explore who introduced which changes to the repository version of the file and when. The annotations view lets you see detailed information for each line of code, such as the version from which this line originated, the ID of the user who committed this line, and the commit date.For more information about annotations, refer to [Locate code author (Annotate with Git Blame)](investigate-changes.html#annotate_blame).  
  
The most useful shortcuts are the following:

Shortcut| Description  
---|---  
`Ctrl+Shift+D`| Use this keyboard shortcut to show the popup menu of the most commonly used diff commands.  
`Ctrl+Shift+Tab`| Use this keyboard shortcut to switch between the left and the right panes.  
`Ctrl+Z`/`Ctrl+Shift+Z`| Use this keyboard shortcut to undo/redo a merge operation. Conflicts will be kept in sync with the text.
