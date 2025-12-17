[//]: # (Source: https://www.jetbrains.com/help/idea/resolving-text-conflicts.html)
[//]: # (Downloaded: 2025-12-17 19:57:42)

# Resolve conflicts in Subversion

If a conflict occurs in a file under the Subversion version control, conflict markers are added to the conflicting file, and three auxiliary unversioned files are created in your local working copy:

  * filename.mine: the copy of your local file without conflict markers.

  * filename.rOld: the base revision you have last synchronized to.

  * filename.rNew: the latest version on the server.




Conflicting files are marked with red in the Commit window. In the [Update Info](version-control-tool-window-update-info-tab.html) tab, they are grouped in the Merged with conflicts list and are also marked with red.

You can resolve conflicts in two ways:

  * Semi-automatically, using a merge tool.

  * Manually in the editor. After that, you need to manually mark the processed files as conflicts-free.




### Resolve a text conflict using the merge tool

  1. In the Version Control tool window `Alt+9`, select the conflicting file: 

![img](https://resources.jetbrains.com/help/img/idea/2025.3/conflictFilesInChangesToolWindow1.png)
  2. On the main VCS menu, or From the context menu of the selection, choose Subversion | Resolve Text Conflict. The Conflicts dialog appears.

  3. If you want to accept the server version and overwrite your local changes, click Accept Theirs. If you want to force your changes to the repository, click Accept Yours. Clicking Merge opens the merge tool, where you can accept or discard each change individually. As a result, the file is automatically marked as resolved, and auxiliary files are deleted. 

You can click the column header to sort the conflicting files by name.

  4. Once the conflicts have been successfully resolved, commit your local version to the repository.




### To resolve a text conflict manually

  1. Open the conflicting file in the editor.

  2. Do one of the following:

     * Edit the contents within the conflict markers as required.

     * Copy one of the auxiliary files on top of your working file.




### Mark a file as resolved

  1. Do one of the following:

     * Select the file in the Project tool window `Alt+1` or in the Version Control tool window `Alt+9`, and choose Subversion, and then choose Mark Resolved from the context menu of the selection.

     * With the conflicting file opened in the editor, right-click the mouse anywhere in the editor tab. From the context menu choose Subversion, and then choose Mark Resolved.

     * From the context menu, choose VCS | Subversion | Mark Resolved..

  2. In the [Mark Resolved](mark-resolved-dialog-subversion.html) dialog that opens select the file.

  3. Click the Mark Resolved button.




22 November 2024

[Lock and unlock files and folders](locking-and-unlocking-files-and-folders.html)[Share directory](sharing-directory.html)
