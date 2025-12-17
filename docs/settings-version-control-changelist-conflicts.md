[//]: # (Source: https://www.jetbrains.com/help/idea/settings-version-control-changelist-conflicts.html)
[//]: # (Downloaded: 2025-12-17 20:02:19)

# Changelists

Use this page to set up how you [group changes into changelists](managing-changelists.html).

Item| Description  
---|---  
Create changelists automatically| Select this option if you want IntelliJ IDEA to create new changelists automatically. For example, on Cherry-pick and Revert commit actions. Also, in Unshelve..., Apply patch..., and Revert... dialogs IntelliJ IDEA will offer you to select a target changelist.  
Allow putting changes within one file into different changelists| Select this option if you work on a few tasks within one file and want to put a few changes within it into different changelists.  
Highlight files from inactive changelists| If you select this checkbox, IntelliJ IDEA shows names of the files belonging to inactive changelists in light-blue font in the editor tabs and in the Project view.  
Show dialog on attempt to edit file from inactive changelist| If you select this option, IntelliJ IDEA displays the Resolve Changelist Conflict dialog on an attempt to modify a file from a non-active changelist.Select one of the following options:

  * Shelve the changes (refer to [Shelve changes](shelving-and-unshelving-changes.html#shelve-unshelve-changes) for more information).
  * Move changes to active changelist: the file will be moved to the active changelist.
  * Switch to changelist: the current changelist will be made active.
  * Ignore: the file will be added to the list of files with ignored conflicts.

  
When an empty changelist becomes inactive| In this section, specify whether you want to remove inactive changelists silently or not. The following options are available:

  * Do nothing: Changelists are not removed as they become inactive.
  * Remove silently: Inactive changelists are automatically removed without confirmation.

  
Highlight files with changelist conflicts| If you select this option, IntelliJ IDEA shows a yellow stripe on top of a file from an inactive changelist, when such file has been modified.It lets you choose one of the possible ways to resolve conflicts:

  * Move file to the active changelist.
  * Switch changelists.
  * Ignore conflicts.

The names of the files belonging to inactive changelists are shown in red font in the editor tabs and in the Project view.  
  
26 June 2025

[Version control settings](settings-version-control.html)[Commit](commit-dialog.html)
