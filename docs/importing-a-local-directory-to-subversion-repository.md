[//]: # (Source: https://www.jetbrains.com/help/idea/importing-a-local-directory-to-subversion-repository.html)
[//]: # (Downloaded: 2025-12-17 19:29:21)

# Import a local directory to Subversion repository

You can import an entire directory to your Subversion repository provided that you have access rights. This is helpful for putting a whole project under version control.

Import to the repository is always available, even if Subversion integration is not enabled for your project.

To import a directory to a Subversion repository, do the following:

  1. Go to VCS | Import into Subversion.

  2. In the [Import into Subversion](import-into-subversion.html) dialog that opens, select the target Subversion repository. If the desired target repository location is not in the list, click the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) button to add it (for more details, refer to [Configure Subversion repository location](configuring-subversion-repository-location.html)). Click Import.

  3. In the Select Path dialog that opens, specify the directory you want to import and click OK.

  4. In the SVN Import Options dialog that opens, check the Import to and Import from paths and specify the following options:

     * Depth: use this list to specify the range of recursion into Subversion subdirectories. The available options are: 

       * working copy: select this option to get files/directories from the repository subtrees that have not been checked out yet.

       * empty: select this option to involve only the current file.

       * files: select this option to involve files from the current folder.

       * immediates: select this option to involve direct children of the current file.

       * infinity: select this option to enable full recursion.

     * Include ignored resources: select this option to include files that have been added to the Subversion ignore list and are not subject to version control into the import.

  5. Optionally, enter a commit message, or select one from the Recent Messages list and click OK.




11 February 2024

[Export information from Subversion repository](exporting-information-from-subversion-repository.html)[Integrate changes to Subversion branch](integrating-changes-to-branch.html)
