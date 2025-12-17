[//]: # (Source: https://www.jetbrains.com/help/idea/integrate-project-dialog-subversion.html)
[//]: # (Downloaded: 2025-12-17 19:29:41)

# Integrate Project dialog (Subversion)

Use this dialog to integrate differences between two branches in the Subversion repository into a local working copy.

Item| Description  
---|---  
Source 1| In this field, specify the URL address of the first branch to compare. If necessary, click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the desired URL from the [Select Repository Location](select-repository-location-dialog-subversion.html) dialog.  
Source 2| In this field, specify the URL address of the second branch to compare. If necessary, click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the desired URL from the [Select Repository Location](select-repository-location-dialog-subversion.html) dialog.  
Revision| For each source, specify the revision to use. The possible options are: 

  * HEAD \- select this option to use the Head revision of the source. The Head revision is suggested by default
  * Specified \- select this option to use a revision different from the Head revision. Specify the required revision in the text field. If necessary, click the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) button and select the revision from the Changes Browser dialog.

  
Based on the sources and revisions you specify, the difference between source 2 and source 1 is calculated and applied to the local working copy.  
Use ancestry| Select this checkbox to take the ancestry of the Source1 and Source2 URLs into consideration when comparing revisions. If the checkbox is not selected, only the contents of the files are compared.  
Try merge, but make no changes| Select this checkbox to enable the `--dry-run` switch of the `svn` command. If this checkbox is not selected, the sources are merged silently.  
Depth| Use this list to specify the range of recursion into subdirectories. The available options are:

  * Empty \- select this option to involve only the current file.
  * Files \- select this option to involve the files in the folder.
  * Immediates \- select this option to involve direct children of the current file.
  * Infinity \- select this option to enable full recursion.

  
  
29 August 2025

[Import into Subversion](import-into-subversion.html)[Integrate to Branch](integrate-to-branch.html)
