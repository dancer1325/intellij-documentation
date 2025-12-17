[//]: # (Source: https://www.jetbrains.com/help/idea/work-with-gitlab-merge-requests.html)
[//]: # (Downloaded: 2025-12-17 20:07:03)

## Manage incoming merge requests

If you are a project maintainer, and you have a GitLab remote configured for your project, you can view and manage incoming merge requests directly from IntelliJ IDEA.

To open the Merge Requests tool window, click ![GitLab icon](https://resources.jetbrains.com/help/img/idea/2025.3/vcs-gitlab.org.jetbrains.plugins.gitlab.expui.gitLabToolWindow.svg) in the tool window bar on the left.

![Merge requests filters](https://resources.jetbrains.com/help/img/idea/2025.3/merge_request_filters.png)

Alternatively, go to Git | GitLab | View Merge Requests in the main menu.

Use the Merge Requests tool window to:

  * Filter requests by state, author, assignee, reviewer, and label.

  * Jump to a merge request on GitLab: right-click a merge request and choose Open Merge Request on GitLab from the context menu.




When you double-click a merge request from the list, you can see the overview and timeline tabs.

![Merge request overview with highlighted options](https://resources.jetbrains.com/help/img/idea/2025.3/merge_request_options.png)

In this view, you can:

  * View the timeline of a selected merge request to track its progression and leave comments for the whole merge request.

  * Select a particular commit to filter the list of changes.

  * Create a local branch based on incoming changes: open a merge request, click the branch with incoming changes, and choose Checkout 'branch name' in the context menu.

  * Investigate branch-related changes in the Log tab of the Git tool window: open a merge request, click the branch with incoming changes, and choose Show 'branch name' in Git Log in the context menu.

This will help you navigate the code related to this merge request, make sure the project builds and the tests pass.




To learn about more options, refer to [Give feedback to a merge request](#review-merge-request).

To make sure you always have the latest information about the merge requests, press `Ctrl+F5`. Alternatively, right-click the necessary merge request and select Refresh List.
