[//]: # (Source: https://www.jetbrains.com/help/idea/integrating-changes-to-from-feature-branches.html)
[//]: # (Downloaded: 2025-12-17 19:29:46)

# Integrate changes to/from feature branches in Subversion

A [Feature Branch](http://martinfowler.com/bliki/FeatureBranch.html) is intended for working on a particular feature. It is normally constituted of data downloaded from the trunk, and is integrated back into the trunk when work on the feature is completed. You can apply all changes or select a subset of changes. IntelliJ IDEA creates a changelist with the merged changes and offers it for commit.

To integrate changes from a branch, do the following:

  1. Open the Version Control tool window `Alt+9` and switch to the [Subversion Working Copies Information tab](subversion-working-copies-information-tab.html).

  2. Click the Merge from link and select the source of changes from the popup menu. The available options are: 

     * trunk: select this option to merge changes from the trunk to the current branch.

     * branches: select this option to apply changes from a specific branch to the current branch. Select the source branch from the Branches popup.

     * tags: select this option to apply changes from a specific branch to the current branch. Select the source branch from the Tags popup.

To edit the list of branches, choose the Configure branches option and update the list of branches in the [Configure Subversion Branches](configure-subversion-branches.html) dialog that opens.

  3. In the Merge from <branch_name> dialog that opens, specify the scope of changes to apply. 

     * To have all changes applied, click the Merge all button.

     * To have a subset of changes applied, click the Select revisions to merge button. In the list of revisions, appoint the revisions to apply changes from by selecting checkboxes next to the desired revisions. To have the selected changes applied, click the Merge selected button.

To have all changes applied regardless of the selection, click the Merge all button.

  4. In the Conflicts dialog, view the list of files where problems occurred during the merge procedure and [resolve the problems](resolving-text-conflicts.html) using the following buttons: 

     * Accept Yours \- click this button to have IntelliJ IDEA force your changes.

     * Accept Theirs \- click this button to have IntelliJ IDEA overwrite your changes.

     * Merge \- click this button to open the merge tool and [resolve the conflicts](resolving-text-conflicts.html) there.




23 February 2024

[Integrate SVN projects or directories](integrating-svn-projects-or-directories.html)[Lock and unlock files and folders](locking-and-unlocking-files-and-folders.html)
