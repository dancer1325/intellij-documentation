[//]: # (Source: https://www.jetbrains.com/help/idea/update-project-dialog-mercurial.html)
[//]: # (Downloaded: 2025-12-17 20:05:04)

# Update Project dialog (Mercurial)

In this dialog, select how you want to synchronize your local repository with the central storage.

Option| Description  
---|---  
Pull| Select this option to pull new changesets from the remote repository to the local one. This option can be deselected if the pull operation is performed by other means, for example via a script. The result is identical with that of running the `hg pull` command.  
Update Strategy| In this section, select the synchronization method. This strategy will be applied to all Mercurial version control roots. The available options are: 

  * Only Update: select this option to apply the [update](http://www.selenic.com/hg/help/update) strategy. The local working directory will be updated to the latest available changeset. The result is identical with that of running the `hg update` command. It is recommended to select this option only if there are no conflicting changes or multiple heads, and if the latest changeset is a descendant or ancestor of the working directory's parent. Otherwise, the update operation will be aborted with errors.
  * Merge: select this option to apply the [merge](http://mercurial.selenic.com/wiki/Merge) strategy. The latest changeset from the central repository will be incorporated into the current tip in your working directory. The result is identical with that of running the `hg merge` command. 
    * Commit after merge without conflicts: select this option if you want to commit the resulting changeset after the merge operation has completed successfully.
  * Rebase: select this option to apply the [rebase](http://mercurial.selenic.com/wiki/RebaseExtension) strategy. Your local changes will be detached, the working directory will be synchronized with the central repository, and then the local changes will be appended on top of the new remote changes. To be able to use this method, you need to enable the Rebase extension in the configuration file for your repository (for more information about creating configuration files, refer to [hgrc](http://www.selenic.com/mercurial/hgrc.5.html)).

  
Do not show this dialog in the future| Select this option to have IntelliJ IDEA update your project silently in the future using the specified update strategy.To invoke this dialog before an update, open the the Version Control | Confirmation settings page `Ctrl+Alt+S`, and then select Update in the Display option dialogs when these commands are invoked area.  
  
11 February 2024

[Tag dialog (Mercurial)](tag-dialog-mercurial.html)[Perforce](using-perforce-integration.html)
