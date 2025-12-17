[//]: # (Source: https://www.jetbrains.com/help/idea/create-and-merge-github-pull-requests.html)
[//]: # (Downloaded: 2025-12-17 19:22:48)

## Create a pull request

  1. In the main menu, go to Git | GitHub | Create Pull Request. The Pull Requests tool window opens with a pull request draft.

![Pull Requests tool window with a new pull request](https://resources.jetbrains.com/help/img/idea/2025.3/pull_requests_tool_window.png)

Alternatively, open the Pull Requests tool window and click ![Plus](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) Create Pull Request in the top-right corner.

After you push changes to the remote repository, IntelliJ IDEA will show you a notification with an option to open a new pull request.

  2. The repository on the left is the base repository that will receive the updates.

Click its name and select the branch to which you want to apply your changes.

![Base repository popup](https://resources.jetbrains.com/help/img/idea/2025.3/base_repo_popup.png)
  3. The repository on the right is the head repository with the changes that will be added to the base repository.

Click its name and select the branch that contains the changes you want to apply.

![Head repo popup](https://resources.jetbrains.com/help/img/idea/2025.3/head_repo_popup.png)

If you have a project that uses [multiple remote repositories](set-up-a-git-repository.html#add-second-remote), you can change the head repository in this popup as well.

  4. Double-click the name of any file to open the Diff view and review the changes you are about to submit.

  5. Specify the name for your pull request in the Title field, and, optionally, provide a description of the changes to be applied through your request.

  6. Optionally, add reviewers, assign your pull request to someone, or add a label to your pull request.

  7. Click Create Pull Request.

If you are not yet ready to push your pull request, you can save it as a draft.

     * Click ![Chevron Down](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.chevronDown.svg) next to the Create Pull Request button.

     * In the menu that opens, select Create Draft Pull Request.

Your pull request will appear in the GitHub repository as a draft. You can come back to it later by choosing Git | GitHub | View Pull Requests in the main menu.




If you have a `pull_request_template.md` file, IntelliJ IDEA should add the template description to your pull requests. For more information about templates, refer to [GitHub documentation](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/creating-a-pull-request-template-for-your-repository).
