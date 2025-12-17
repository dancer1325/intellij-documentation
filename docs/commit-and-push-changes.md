[//]: # (Source: https://www.jetbrains.com/help/idea/commit-and-push-changes.html)
[//]: # (Downloaded: 2025-12-17 19:21:08)

## Commit changes locally

  1. Open the vertical Commit tool window `Alt+0` located on the left:

![Commit tool window](https://resources.jetbrains.com/help/img/idea/2025.3/ij_VCS_commit_tool_window.png)
  2. As your changes are ready to be committed, select the corresponding files or an entire changelist.

If you press `Ctrl+K`, the entire active changelist will be selected.

You can also select files under the Unversioned Files node — IntelliJ IDEA will stage and commit these files in one step.

  3. If you want to [append local changes to the latest commit](edit-project-history.html#amend-commit) instead of creating a separate commit, select the Amend option.

  4. Enter the commit message. You can click ![Commit message history button](https://resources.jetbrains.com/help/img/idea/2025.3/app.vcs.history.svg) to choose from the list of recent commit messages.

You can also [edit the commit message](edit-project-history.html#reword-commit) later before you've pushed the commit.

You can customize commit message rules on the Version Control | Commit settings page `Ctrl+Alt+S`. There is also a quick-fix and the Reformat action that wrap a long line or reformat the message.

You can also define a commit template that will be used as the default commit message. Specify the boilerplate text you want to use in a .txt file and execute the following command in the terminal to add it to your Git config: `git config --local commit.template <path_to_template_file>`

  5. If you need to perform commit checks, upload files to a server after the commit, or commit with advanced options, click ![the Gear icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) in the bottom-right corner or press `Ctrl+O`:

![advanced commit options popup](https://resources.jetbrains.com/help/img/idea/2025.3/ij_VCS_advanced_commit_options.png)

The following options are available:

     * Author: if you are committing changes made by another person, you can specify the author of these changes.

     * Sign-off commit: select if you want to sign off your commit to certify that the changes you are about to check in have been made by you, or that you take the responsibility for the code you are committing. 

When this option is enabled, the following line is automatically added at the end of the commit message: Signed off by: <username>

     * In the Commit Checks area, select the actions you want IntelliJ IDEA to perform before committing the selected files to the local repository.

The following options are available:

       * Reformat code: perform code formatting according to the [Project Code Style settings](settings-code-style.html).

       * Rearrange code: rearrange your code according to the [arrangement rules preferences](reformat-and-rearrange-code.html).

       * Optimize imports: remove redundant import statements.

       * Cleanup: batch-apply quick-fixes from code cleanup inspections. Click Choose profile to select a [profile](customizing-profiles.html) from which the IDE will run inspections.

       * Update copyright: add or update a copyright notice according to the selected copyright profile - scope combination.

       * Check malicious dependencies: search for [malicious NPM and PyPI dependencies](package-analysis.html#malicious-dependencies) that might be declared in your project.

     * In the Advanced Commit Checks area, the following options are available:

       * Run advanced checks after a commit is done: enable this option to run the selected advanced commit checks after a commit is done.

With this option enabled, if some of the advanced commit checks fail, the changes will be committed anyway.

Note that if you want to Commit and Push (`Ctrl+Alt+K`) your changes right away, the checks will be done before the commit.

Also, this option is not available for the modal commit interface.

       * Analyze code: analyze modified files while committing them. Click Choose profile to select an [inspection profile](customizing-profiles.html) from which the IDE will run inspections.

       * Check TODO: Review the [TODO items](using-todo.html) matching the specified filter. Click Configure to choose an [existing TODO filter](using-todo.html), or open the [TODO settings page](settings-todo.html) and define a new filter to be applied.

       * Run Tests: [run tests as commit checks](performing-tests.html#run-tests-after-commit). Click Choose configuration near Run Tests and select which configuration you want to run.

     * In the After Commit area, you can select the [server access configuration](configuring-synchronization-with-a-remote-host.html) or a [server group](server-groups.html) to use for uploading the committed files to a local or remote host, a mounted disk, or a directory. For more information, refer to [Deployment](deploying-applications.html). 

The following options are available:

       * Upload files to: select the [server access configuration](configuring-synchronization-with-a-remote-host.html) or a [server group](server-groups.html) to use for uploading the committed files to a local or remote host, a mounted disk, or a directory. 

         * To suppress uploading, choose None.

         * To add a server configuration to the list, click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and fill in the required fields in the Deployment dialog that opens.

The list is only available if the FTP/SFTP/WebDAV Connectivity plugin is enabled.

       * Always use selected server or group of servers: always upload files to the selected [server](configuring-synchronization-with-a-remote-host.html) or a [server group](server-groups.html).

The checkbox is only available if the FTP/SFTP/WebDAV Connectivity plugin is enabled.

  6. When you're ready, click Commit or Commit and Push (`Ctrl+Alt+K`) to push the changes to the remote repository immediately after the commit. You will be able to review the current commit as well as all other commits before they are pushed to the remote.




If there are [Git hooks](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks) stored in `.git/hooks`, they are executed automatically during commit operations.

You can disable running Git hooks for a particular commit in the [commit settings](#commit_settings) by clearing the Run Git hooks checkbox.

To disable this option on the IDE level, go to Settings | Advanced settings | Version Control. Git and select the Do not run Git commit hooks checkbox.

If you want to commit local changes in a separate modal commit dialog, go to Settings | Advanced Settings | Version Control to enable the [Modal Commit Interface plugin](https://plugins.jetbrains.com/plugin/26647-modal-commit-interface).

Also, check the options to [customize the commit tool window behavior](#customize-changes-review).

### Commit part of a file

Sometimes when you make changes that are related to a specific task, you also apply other unrelated code modifications that affect the same file. Including all such changes into one commit may not be a good option, since it would be more difficult to review, [revert](undo-changes.html#revert-commit), [cherry-pick](apply-changes-from-one-branch-to-another.html#cherry-pick) them, and so on.

IntelliJ IDEA lets you commit such changes separately in one of the following ways:

  * [select modified code chunks and lines](#select_chunks_in_commit_changes_dialog) that you want to include in a commit right in the Commit Changes dialog and leave other changes pending so that you can commit them later.

  * [put different code chunks into different changelists](#put_changes_into_different_changelists) on the fly, when you edit code, and then commit these changelists separately.

You can also create a new changelist and [make it active](managing-changelists.html), then all changes that you make after that will fall into that changelist, while any modifications you made before that will stay where they are.




### Select chunks and specific lines you want to commit

  1. Open the Commit tool window `Alt+0`.

  2. To display the differences between the repository version and the local version of the selected file, in the Commit tool window `Alt+0`, click ![the Diff icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.vcs.diff.svg) on the toolbar or press `Ctrl+D`.

  3. Select the checkbox next to each chunk of modified or newly added code that you want to commit, and leave other changes unselected:

![Partial commit dialog](https://resources.jetbrains.com/help/img/idea/2025.3/partial_commit_dialog.png)

You can also select Move to Another Changelist from the context menu of a modified chunk to split changes between different changelists that you can commit separately.

To assign a custom shortcut for this action, look for the Move Lines to Another Changelist action under Version Control Systems on the Keymap settings page `Ctrl+Alt+S`.

  4. If you want to commit only a specific line from a chunk, right-click the line you want to include and select Split Chunks and Include Selected Lines into Commit.

![IntelliJ IDEA: An option to include current line in commit in the context menu](https://resources.jetbrains.com/help/img/idea/2025.3/include_line_to_commit.png)

Alternatively, hover over the gutter and select or clear the checkbox next to the line you want to include in the commit or exclude from it.

  5. Click Commit. Unselected changes will stay in the current changelist, so that you can commit them separately.




### Commit selected changes from the editor

If you have already committed your changes and then realized you have forgotten something, you can quickly commit any updates right from the editor.

  1. When you make a change to a file in the editor, click the corresponding [change marker](adding-files-to-version-control.html#track_changes) in the gutter.

If there are no change markers in the gutter, make sure the Highlight modified lines in the gutter option is enabled on the Version Control | Confirmation | Gutter settings page `Ctrl+Alt+S`.

  2. In the toolbar that appears, write the commit message and click ![](https://resources.jetbrains.com/help/img/idea/2025.3/intellij.platform.vcs.impl.icons.CommitInline.svg) Commit this change.

![Inline commit field](https://resources.jetbrains.com/help/img/idea/2025.3/inline_commit.png)

Click ![](https://resources.jetbrains.com/help/img/idea/2025.3/intellij.platform.vcs.impl.icons.AmendInline.svg) Amend in the commit message field to append the local changes to the latest commit.




### Put changes into different changelists

  1. When you make a change to a file in the editor, click the corresponding [change marker](adding-files-to-version-control.html#track_changes) in the gutter.

If there are no change markers in the gutter, make sure the Highlight modified lines in the gutter option is enabled on the Version Control | Confirmation | Gutter settings page `Ctrl+Alt+S`.

  2. In the toolbar that appears, select the target changelist for the modified code chunk (or create a new changelist):

![Partial commit changelists](https://resources.jetbrains.com/help/img/idea/2025.3/partial_commit_changelists.png)
  3. Commit each changelist separately.




### Customize the way you review the local changes

IntelliJ IDEA has different settings to customize your workflow for reviewing the local changes before commit.

### Customize the commit tool window

The location and behavior of the Commit tool window `Alt+0` can be changed based on your preferred workflow.

  * The commit interface can be opened as a separate window that would look like a dialog, but would still be non-blocking (or non-modal).

In the Commit tool window `Alt+0`, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moreVertical.svg) Options and select View Mode | Window. To always keep the window in front of the IDE, select View Mode | Float.

If you do not want the Commit tool window to close after you commit your changes, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moreVertical.svg) Options and clear the Close Tool Window After Committing option.

Alternatively, in Settings | Advanced settings | Version Control, clear the Automatically close the Commit tool window in Window/Float mode after committing checkbox.

  * You can set up the Commit tool window to work as a window with a list of local changes and switch on the commit controls (with ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.toolwindows.commit.png) Commit or `Ctrl+K`) when you are ready to commit your changes.

In Settings | Advanced settings |Version Control, select the Toggle commit controls checkbox.

  * The Commit tool window can become the Local changes tab in the Log tab of the Git tool window `Alt+9`.

In Settings | Advanced settings | Version Control, clear the Enable Commit tool window checkbox.




If you switch on the Toggle commit controls option and switch off the Enable Commit tool window option, this is what the Commit tab will look like:

[![Git tool window with the Commit tab, toggle mode on](https://resources.jetbrains.com/help/img/idea/2025.3/commit_tab_toggle_mode.png)](https://resources.jetbrains.com/help/img/idea/2025.3/commit_tab_toggle_mode.png)

### Customize Diff Viewer behavior

  1. In the Commit tool window `Alt+0`, there is a list of changed files. The double click on the changed file can either open the Diff Viewer or the source file.

Click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moreVertical.svg) Options, select Show on Double-Click and then the preferred option:

     * Diff to always open the Diff Viewer when you double-click the changed file so that you could review the changes.

     * Source to always open the file itself so that you could edit it.

  2. You can also set up the Diff Viewer to open in the editor or in a separate window with one of these settings:

     * In the Diff Viewer, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) Settings on the toolbar and select Show Diff in Separate Window.

     * In Settings | Advanced Settings | Version Control, clear the Open Diff as Editor Tab checkbox.




### Use the Git staging area to commit changes

If you are more used to the concept of [staging](https://git-scm.com/docs/git-add) changes for commit instead of using [changelists](managing-changelists.html) where modified files are staged automatically, press `Ctrl+Alt+S` to open settings and select Version Control | Git, then select the Enable staging area checkbox.

The Commit tool window will now look as follows:

![Git staging area](https://resources.jetbrains.com/help/img/idea/2025.3/git_staging_area.png)

Using the staging area allows you to easily commit changes to the same file separately (including overlapping changes), and see which changes are already staged without switching focus from the editor.

When you switch from using changelists to Git staging area, all existing changelists are saved. You can switch between the two modes without losing your changes.

### Stage changes for commit

  1. Do one of the following:

     * To stage an entire file, in the Commit tool window `Alt+0`, select this file and click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) on the right next to it or press `Ctrl+Alt+A`.

![Stage from the Commit tool window](https://resources.jetbrains.com/help/img/idea/2025.3/git_stage_from_toolwindow.png)
     * To stage a specific chunk inside a file, in the editor click the [change marker](adding-files-to-version-control.html#track_changes) in the gutter next to the modified chunk and click Stage.

![Stage change from the editor](https://resources.jetbrains.com/help/img/idea/2025.3/git_stage_from_editor.png)

Staged changes (including changes staged from outside IntelliJ IDEA) are marked with a hollow change marker in the editor:

![Gutter marker for staged changes](https://resources.jetbrains.com/help/img/idea/2025.3/git_staged_marker.png)
     * To stage granular changes like a single line instead of a code chunk, or even one of several changes to a single line, in the Commit tool window `Alt+0`, select the file containing the change and choose Compare HEAD, Staged and Local Versions from the context menu.

This will open a three-way [Diff Viewer](differences-viewer.html) where the left pane shows the repository version, the right pane shows the local version, and the central pane is a fully-functional editor where you can make the changes you want to stage.

![Stage changes interactively](https://resources.jetbrains.com/help/img/idea/2025.3/git_stage_interactively.png)
  2. When ready, commit the changes as described in [Commit changes locally](#commit_tool_window).



