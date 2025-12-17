[//]: # (Source: https://www.jetbrains.com/help/idea/comparing-files-and-folders.html)
[//]: # (Downloaded: 2025-12-17 19:21:16)

## Compare files

### Compare two or three files

  * In the Project tool window `Alt+1`, select the files you want to compare and choose Compare Files, or press `Ctrl+D`.

  * Alternatively, select one file, choose Compare With from its context menu, and select a file that is outside your project.




If you are comparing two files and want to add a third file to the comparison, right-click either left or right panel, select Switch to Three-Side Viewer, and load the required file by clicking Select file.

### Compare active editor with Clipboard

  * Right-click anywhere in the editor and choose Compare with Clipboard from the context menu.




### Compare active editor with a project file

  1. In the Project tool window `Alt+1`, right-click the file you want to compare with the currently opened file.

  2. Choose Compare File with Editor from the context menu. 




### Compare active editor with any file

If you often need to compare files that are outside your project with the active editor, or don't want to have the Project tool window `Alt+1` open, you can use the Compare File with Editor action that lets you choose any file and compare it with the active editor.

To add this action to the editor tab's context menu:

  1. Press `Ctrl+Alt+S` to open settings and then select Appearance & Behavior | Menus and Toolbars.

  2. In the right pane, expand the Editor Tab Popup Menu node, select where you want to add the new action, click ![the Add Actions menu](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select Add Action.

  3. Find and add the Compare File with Editor action under Version Control Systems | Diff & Merge.




### Compare a local file with its repository version

  1. Open the Commit tool window `Alt+0`. 

  2. Locate the required file in a changelist and do one of the following:

     * Right-click the file and select Git | Show Diff.

     * Select the file and press `Ctrl+D`.

     * Double-click the file.




IntelliJ IDEA displays the differences in the [Diff Viewer for Files](differences-viewer.html):

![Comparing files in IntelliJ IDEA diff viewer](https://resources.jetbrains.com/help/img/idea/2025.3/ij_compareFiles.png)

Color| Description  
---|---  
![New lines](https://resources.jetbrains.com/help/img/idea/2025.3/diff_new_lines_color.png) Green| Added  
![Modified lines](https://resources.jetbrains.com/help/img/idea/2025.3/diff_changed_lines_color.png) Blue| Modified  
![Deleted lines](https://resources.jetbrains.com/help/img/idea/2025.3/diff_deleted_lines_color.png) Gray| Deleted  
  
To apply changes, use the chevron buttons: ![apply left](https://resources.jetbrains.com/help/img/idea/2025.3/app.diff.applyNotConflictsLeft.svg) and ![apply right](https://resources.jetbrains.com/help/img/idea/2025.3/app.diff.applyNotConflictsRight.svg).

To append changes, press `Ctrl` — the ![apply left](https://resources.jetbrains.com/help/img/idea/2025.3/app.diff.applyNotConflictsLeft.svg) ![apply right](https://resources.jetbrains.com/help/img/idea/2025.3/app.diff.applyNotConflictsRight.svg) buttons will turn into ![chevron button bottom right](https://resources.jetbrains.com/help/img/idea/2025.3/app.diff.arrowRightDown.svg) ![chevron button bottom left](https://resources.jetbrains.com/help/img/idea/2025.3/app.diff.arrowLeftDown.svg).

### Productivity tips

Assign shortcuts for 'accept' and 'append'
    

To assign shortcuts to the accept and append actions, open the Keymap settings page `Ctrl+Alt+S` and locate these actions under Version Control Systems | Diff & Merge.

Swap sides
    

When you are comparing two files, or a file with the Clipboard contents, you can swap sides by clicking ![the Swap Sides button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.swapPanels.svg) on the toolbar.

Compare files from the command line
    

You can compare two or three files from the command line and use IntelliJ IDEA as an external diff tool. For more information, refer to [Compare files from the command line](command-line-differences-viewer.html). 
