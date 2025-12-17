[//]: # (Source: https://www.jetbrains.com/help/idea/update-project-dialog-subversion.html)
[//]: # (Downloaded: 2025-12-17 20:05:06)

# Update Project dialog (Subversion)

Use this dialog to update the local working copy of a file, directory, or project with a revision from the repository.

Item| Description  
---|---  
Update/Switch to specific Url| 

  * Select this checkbox to synchronize your local working copy with a specific repository. Specify the source repository either in the URL field through its full Url address or in the Use Branch field through the branch name.
  * Clear this checkbox to bring the changes from the repository that corresponds to the current working copy.

  
Use Branch| In this field, specify the location of the required repository through its branch name. Click Browse ![Browse](https://resources.jetbrains.com/help/img/idea/2025.3/browseButton.png) to choose the required branch in the [Select Branch](select-branch.html) dialog that opens. 

  1. To use this method of specifying the required repository, you need to [configure a list of branches](configuring-subversion-branches.html) you work with. If you have not done it yet, click Configure Branches in the Select Branch dialog.
  2. The field is enabled only when the Update/Switch to specific Url checkbox is selected.

  
Url| In this field, specify the location of the required repository through its full URL address. Click Browse ![Browse](https://resources.jetbrains.com/help/img/idea/2025.3/browseButton.png) to open the [Select Repository Location](select-repository-location-dialog-subversion.html) dialog. The field is enabled only when the Update/Switch to specific Url checkbox is selected.  
Update/Switch to specific revision| Select this checkbox to synchronize your local working copy with a specific revision different from the HEAD revision. The Update/Switch to specific revision field becomes enabled.In this field, specify the number of the revision to be used. Click Browse ![Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/browseButton.png) to open the Changes Browser dialog. By default, IntelliJ IDEA suggests to update your local working copy the HEAD revision. This option corresponds to the `--non-recursive (-N)` switch of the Subversion `update` command.  
Depth| Use this list to specify the range of recursion into subdirectories. The available options are: 

  * Working copy \- select this option to get files/directories from repository subtrees that have not been checked out yet.
  * Empty: select this option to involve only the current file.
  * Files: select this option to involve the files in the folder.
  * Immediates: select this option to involve direct children of the current file.
  * Infinity: select this option to enable full recursion.

  
Force Update| Select this checkbox to have local files replaced with the files from the repository even if the local files have modifications and thus abandon the local modifications.  
Ignore Externals| Select this checkbox if you do not want IntelliJ IDEA take into account [externals definitions](http://svnbook.red-bean.com/en/1.7/svn-book.html#svn.advanced.externals) during update.  
Do not show this dialog in the future| Select this checkbox to have IntelliJ IDEA perform future updates silently. To have IntelliJ IDEA show this dialog before update again:

  1. Open the [Version Control - Confirmation](settings-version-control-confirmation.html) page of the [Settings](settings-preferences-dialog.html) field.
  2. In the Display Option dialogs when these commands are invoked area, select the Update checkbox.

  
  
29 August 2025

[SVN Repositories](svn-repositories.html)[Version control integration support](enabling-version-control.html)
