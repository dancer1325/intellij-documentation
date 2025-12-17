[//]: # (Source: https://www.jetbrains.com/help/idea/checking-out-files-from-subversion-repository.html)
[//]: # (Downloaded: 2025-12-17 19:19:52)

# Check out files from Subversion repository

By checking out files from a Subversion repository, you obtain a [local working copy of the repository](configuring-the-format-of-the-local-working-copy.html), which you can edit. After making the necessary changes, you can publish the results by committing, or checking in your changes to the repository.

  1. In the main menu, go to VCS | Get from Version Control.

  2. In the [Get from Version Control](check-out-from-subversion-dialog.html) dialog, click Add Repository Location and specify the repository URL.

  3. Click Check Out.

  4. In the dialog that opens, specify the destination directory where the local copy of the repository files will be created, and click OK.

If you are checking out sources for an existing project, the destination folder should be below the project content root.

  5. In the SVN Checkout Options dialog, specify the following settings:

     * Revision to be checked out (HEAD or a selected revision).

     * Whether you need to check out the nested directories.

     * Whether you need to include the external locations.

Click OK.




This action is also available from the [SVN Repositories tool window](svn-repositories.html). Right-click a directory and choose the required command from the context menu.

IntelliJ IDEA suggests creating a project based on the sources checked out from version control.

08 October 2024

[Browse Subversion repository](browsing-subversion-repository.html)[Clean up local working copy](cleaning-up-local-working-copy.html)
