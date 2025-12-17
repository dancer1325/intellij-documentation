[//]: # (Source: https://www.jetbrains.com/help/idea/update-project-dialog-perforce.html)
[//]: # (Downloaded: 2025-12-17 20:05:05)

# Update Project dialog (Perforce)

Use this dialog to update the local working copy of a file, directory, or project with a revision from the repository.

Item| Description  
---|---  
Revert unchanged files before sync (p4 revert -a)| Select this checkbox to discard changes made to open files. This option corresponds to the Perforce `revert` command. For more information, refer to [p4 revert](http://maillist.perforce.com/perforce/doc.091/manuals/cmdref/revert.html#1040665) reference.  
Force sync (-f)| Select this checkbox to forcibly copy files from the depot into the workspace. This option corresponds to the Perforce `sync` command. For more information, refer to [p4 sync](http://maillist.perforce.com/perforce/doc.091/manuals/cmdref/sync.html#1040665) reference.  
Run resolve automatically after the sync (p4 resolve -am)| Select this checkbox to resolve conflicts between file revisions. This option corresponds to the Perforce `resolve` command. For more information, refer to [p4 resolve](http://maillist.perforce.com/perforce/doc.091/manuals/cmdref/resolve.html#1040665) reference.  
Do not show this dialog in the future| If this checkbox is selected, the specified actions will be performed silently in future.  
  
29 August 2025

[Perforce Options dialog](perforce-options-dialog.html)[Subversion](using-subversion-integration.html)
