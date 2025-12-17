[//]: # (Source: https://www.jetbrains.com/help/idea/adding-files-to-local-mercurial-repository.html)
[//]: # (Downloaded: 2025-12-17 19:17:51)

# Add files to a local Mercurial repository

After a Mercurial repository for a project is [initialized](setting-up-a-local-mercurial-repository.html), you need to add the project data to it:

  * If you have specified [enabled Mercurial for your project](using-mercurial-integration.html#enable-mercurial-integration), IntelliJ IDEA suggests putting each new file under Mercurial control during the file creation.

  * You can add all unversioned files to Mercurial control or select files to add.




### Add all unversioned files to Mercurial

  1. Open the Commit tool window `Alt+0`. 

  2. Right-click the Unversioned Files node and choose Add to VCS from the context menu.

  3. Click Commit or press `Ctrl+K`.




### Add specific file(s) to Mercurial

  1. Open the Commit tool window `Alt+0`. 

  2. Expand the Unversioned Files node, select the files to be added. From the context menu, choose Add to VCS.

You can also add files to VCS from the Project tool window `Alt+1`: right-click the files that you want to add and select Mercurial | Add.

  3. Click Commit or press `Ctrl+K`.




### Specify the commit options

In IntelliJ IDEA, you can run commit checks, upload files to a server after the commit, or commit with advanced options.

  1. Open the Commit tool window `Alt+0` and click ![Show Commit Options](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) in the bottom-right corner.

  2. Select the necessary options:

![advanced commit options popup](https://resources.jetbrains.com/help/img/idea/2025.3/ij_VCS_advanced_commit_options_hg.png)
     * In the Before Commit area, select the actions you want IntelliJ IDEA to perform before committing the selected files to the local repository.

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




22 November 2024

[Set up a local Mercurial repository](setting-up-a-local-mercurial-repository.html)[Manage Mercurial branches and bookmarks](managing-mercurial-branches-and-bookmarks.html)
