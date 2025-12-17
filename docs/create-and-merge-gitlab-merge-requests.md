[//]: # (Source: https://www.jetbrains.com/help/idea/create-and-merge-gitlab-merge-requests.html)
[//]: # (Downloaded: 2025-12-17 19:22:50)

## Create a merge request

  1. In the main menu, go to Git | GitLab | View Merge Requests.

  2. In the Merge Requests tool window that opens, click ![Plus](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) Create Merge Request in the top-right corner.

A new tab opens with a merge request draft.

![Merge Requests tool window with a new merge request](https://resources.jetbrains.com/help/img/idea/2025.3/merge_requests_tool_window.png)

After you push changes to the remote repository, IntelliJ IDEA will show you a notification with an option to open a new merge request.

  3. Click the name of the base repository on the left and specify the branch that will receive the updates. 

![Base repository](https://resources.jetbrains.com/help/img/idea/2025.3/mr_base_repo.png)
  4. Click the name of the head repository on the right and specify the branch with the changes that will be added to the base repository.

![Head repository](https://resources.jetbrains.com/help/img/idea/2025.3/mr_head_repo.png)

If you have a project that uses [multiple remote repositories](set-up-a-git-repository.html#add-second-remote), you can change the head repository in this popup as well.

  5. Specify the name for your merge request in the Title field, and, optionally, provide a description of the changes to be applied through your request and add reviewers.

  6. Click Create Merge Request.



