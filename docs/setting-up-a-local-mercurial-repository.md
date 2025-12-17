[//]: # (Source: https://www.jetbrains.com/help/idea/setting-up-a-local-mercurial-repository.html)
[//]: # (Downloaded: 2025-12-17 20:00:21)

# Set up a local Mercurial repository

Although Mercurial provides high flexibility in arranging data and your work with repositories, the following scenarios are most commonly used for setting up a local Mercurial repository:

  * [Clone](#cloneExistingRepository) an existing remote repository and create a new project with the downloaded data.

  * [Create a local repository](#createNewRepository) which you can push to a remote location later, if necessary.




### Clone a remote Mercurial repository

  1. Go to Hg | Get from Version Control.

The Get from Version Control dialog opens.

  2. In the dialog that opens, select Mercurial from the Version control list and specify the URL of the remote repository you want to clone.

  3. Click Clone. If you want to create an IntelliJ IDEA project based on the sources you have cloned, click Yes in the confirmation dialog.




### Create a local Mercurial repository

  1. Open the project you want to store in a repository.

  2. In the main menu, go to Hg | Create Mercurial Repository.

  3. Specify the location of the new repository.

When the repository has been created, you will see a notification.

![Notification saying that the             Mercurial repository has been created](https://resources.jetbrains.com/help/img/idea/2025.3/mercurial_repository_created_notification.png)
  4. Put the required files under Mercurial version control. The uncommitted files appear in the Commit to <branch name> tab of the Commit tool window (`Alt+0`).

Note that if you specify Mercurial as the version control system for a directory in the [Version control settings](settings-version-control.html) dialog, IntelliJ IDEA will suggest to put each new file in this directory under Mercurial control.




Mercurial does not support external paths. So if you choose another directory, note that it must contain the tree where the project root resides.

If you choose a directory which is already under Mercurial control, IntelliJ IDEA opens the Directory Is Under hg dialog, where you can choose to create a repository in the specified location or to stay in the parent repository.

11 February 2024

[Mercurial](using-mercurial-integration.html)[Add files to a local Mercurial repository](adding-files-to-local-mercurial-repository.html)
