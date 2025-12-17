[//]: # (Source: https://www.jetbrains.com/help/idea/using-patches.html)
[//]: # (Downloaded: 2025-12-17 20:05:35)

# Use patches

Instead of committing your local changes, you can put them in a .patch file that you can apply to your sources later, send by email, and so on. Using patches is a convenient mechanism for sharing changes without checking them in a Git repository.

### Create a patch from uncommitted changes

  1. In the Commit tool window `Alt+0`, select the file or changelist that you want to include in the patch, and choose Create Patch from Local Changes from the context menu.

  2. In the dialog that opens, make sure that all the changes you want to include in the patch are selected, enter a commit comment (it will be used as the patch file name), and click Create Patch.

  3. In the Patch File Settings dialog, specify the following details:

     * The patch file location: choose the default location or select the To clipboard option if you do not want to save the patch to a file.

     * Base path: specify the path relative to which paths inside the patch file will be written. Normally, this is your project directory, but you may want to use a relative path, for example, if the modified files are stored inside your Git repository.

     * Reverse patch: select this option if you want to create a patch that reverts the changes you have made.

     * Encoding: select the encoding for the patch file from the drop-down list.




If you do not need to save the patch to a file (for example, you want to send it by email instead), right-click the necessary file(s) in the Commit tool window `Alt+0` and choose Copy as Patch to Clipboard from the context menu.

### Create a patch from an entire commit

  1. In the Log tab of the Git tool window `Alt+9`, locate the commit with the changes you want to include in the patch and select Create Patch from the context menu.

  2. In the Patch File Settings dialog, specify the following details:

     * The patch file location: choose the default location or select the To clipboard option if you do not want to save the patch to a file.

     * Base path: specify the path relative to which paths inside the patch file will be written. Normally, this is your project directory, but you may want to use a relative path, for example, if the modified files are stored inside your Git repository.

     * Reverse patch: select this option if you want to create a patch that reverts the changes you have made.

     * Encoding: select the encoding for the patch file from the drop-down list.




### Create a patch from a file

  1. Select the necessary file in any view (the Project tool window `Alt+1`, the editor, the Commit window, and so on).

  2. Select Git | Selected File | Show History from the main menu or Git | Show History from the context menu of the selection. The History tab is added to the Git tool window showing the history for the selected file and allowing you to review and compare its revisions.

  3. Right-click a revision and choose Create Patch from the context menu.




### Apply patches

  1. Select Git | Patch | Apply patch from the main menu.

  2. In the Apply Patch dialog that opens, specify the path to the .patch file you want to apply.

You can drag a file or an email attachment to any place in the editor.

  3. If necessary, click ![the folders icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.vcs.folders.svg) and choose Map Base Directory to specify a directory relative to which file names in the patch file will be interpreted. You can map the base directory to a single file, directory, or selection.

  4. If the source code was edited after a patch was created, conflicts may arise. To check if your patch can be applied without conflicts, click Show Diff ![the Show diff icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.vcs.diff.svg) `Ctrl+D`. If there are conflicts, the corresponding lines will be highlighted in red.

  5. If you want to apply changes to files stored in different locations than those specified in the patch, you can strip off the leading directories by clicking ![the folders icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.vcs.folders.svg) and choosing Remove All Leading Directories.

  6. Select the changelist to which you want to apply the patch or specify the name of a new changelist in the Name field, and enter a comment to this changelist (optionally).

  7. If you want to make this changelist active, select the Set active option.

  8. If you want IntelliJ IDEA to save the context of a task associated with the new changelist when deactivated and restore the context when the changelist becomes active, select the Track context option (refer to [tasks and contexts](managing-tasks-and-context.html) for details) .

  9. If you want to move the patch to a temporary storage (shelf) before applying it, click Import to shelf (for more information, refer to [Shelve or stash changes](shelving-and-unshelving-changes.html)). Otherwise, click OK.




You can also copy the content of a patch file and apply it by choosing Git | Apply Patch from Clipboard from the main menu. For example, this is convenient when you receive a patch by email and do not want to save it. For [Git format](https://git-scm.com/docs/git-format-patch) patches, IntelliJ IDEA extracts the commit message and the author and automatically fills the corresponding fields in the Commit tool window `Alt+0`.

04 September 2025

[Shelve or stash changes](shelving-and-unshelving-changes.html)[Undo changes in Git repository](undo-changes.html)
