[//]: # (Source: https://www.jetbrains.com/help/idea/integrating-changes-to-branch.html)
[//]: # (Downloaded: 2025-12-17 19:29:45)

# Integrate changes to Subversion branch

IntelliJ IDEA allows you to integrate changes into a selected branch, and commit the results of such integration to the repository. Do the following:

  1. In the Version Control tool window `Alt+9`, switch to the [Repository tab](version-control-tool-window-repository-and-incoming-tabs.html).

  2. Right-click the changelist you want to integrate, and select Subversion | Integrate to Branch from the context menu: 

![svnIntegrateToBranch.png](https://resources.jetbrains.com/help/img/idea/2025.3/svnIntegrateToBranch.png)

If you want to integrate separate files instead of the whole changelist, select them in the Changed Files pane and choose Subversion | Integrate To Branch from the context menu.

If you are using SVN 1.5 or later both on the server and in your local working copy, select the relevant changelist/file(s) in the Changelists or Changed Files pane and click ![integrateToBranch.png](https://resources.jetbrains.com/help/img/idea/2025.3/integrateToBranch.png) on the toolbar.

![svnIntegrateFilesToBranch.png](https://resources.jetbrains.com/help/img/idea/2025.3/svnIntegrateFilesToBranch.png)

The [Integrate to Branch](integrate-to-branch.html) dialog opens displaying the URL addresses of the source and target branches and a list of available local working copies.

  3. From the Integrate into working copy list, select the path to the local working copy into which the selected changelist will be integrated. 

To add a path to the list, click the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) button.

To remove a path from the list, click the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) button.

Make sure the specified working copy directory is under Subversion version control!

  4. To preview the merge result by enabling the `--dry-run` switch of the `svn` command, select the Try merge, but make no changes checkbox. 

If this checkbox is not selected, sources are merged silently.

  5. Click OK. The Commit Changes dialog opens.

  6. Review the summary, specify the necessary options, and run commit.




30 September 2025

[Import a local directory to Subversion repository](importing-a-local-directory-to-subversion-repository.html)[Integrate SVN projects or directories](integrating-svn-projects-or-directories.html)
