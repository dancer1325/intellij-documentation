[//]: # (Source: https://www.jetbrains.com/help/idea/manage-projects-hosted-on-github.html)
[//]: # (Downloaded: 2025-12-17 19:31:45)

## Check out a project (clone)

You can clone a [repository](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/about-repositories) that you want to contribute to directly from IntelliJ IDEA and create a new project based on it.

  1. In the main menu, go to Git | Clone. If the Git menu is not available, choose VCS | Get from Version Control.

  2. In the Get from Version Control dialog, choose GitHub on the left.

  3. Log in to GitHub by doing one of the following:

     * If you have a token, click Use token, then paste the token in the Token field, and click Log In.

     * Otherwise, click Log In via GitHub.

Enter your GitHub credentials in the browser window that opens. If you have [two-factor authentication](https://blog.github.com/2013-09-03-two-factor-authentication/) enabled, you will be asked to enter a code that will be sent to you by SMS or through the mobile application.

For more information about managing your GitHub accounts, refer to [Add your GitHub account](set-up-a-github-account.html#register-account).

  4. Select a repository from the list of all GitHub projects associated with your account and the organization that your account belongs to. 

  5. In the Directory field, enter the path to the folder where your local Git repository will be created.

  6. If you want to perform [shallow clone](https://git-scm.com/docs/git-clone#Documentation/git-clone.txt-code--depthcodeemltdepthgtem) with a limited history, select the Shallow clone with a history truncated to checkbox and specify the number of commits that you want to clone.

You can fetch the rest of the history later by selecting Git | Unshallow Repository in the main menu.

  7. Click Clone.

If you want to create a project based on these sources, click Yes in the confirmation dialog. IntelliJ IDEA will automatically set Git root mapping to the project root directory.



