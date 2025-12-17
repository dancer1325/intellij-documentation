[//]: # (Source: https://www.jetbrains.com/help/idea/log-tab.html)
[//]: # (Downloaded: 2025-12-17 19:31:39)

## Branches Pane

The Branches pane lists all local and remote branches, and lets you perform all branch operations.

### Branches pane toolbar

Icon| Action| Description  
---|---|---  
![the Left arrow icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.chevronLeft.svg)| Hide Git Branches| Hide the Branches pane.  
![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| New Branch| [Create a new branch based on the selected branch](manage-branches.html#create-branch-from-selected).  
![the Update Selected button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.vcs.update.svg)| Update Selected| [Fetch](sync-with-a-remote-repository.html#fetch) changes from the selected branch.  
![the Delete button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.delete.svg)| Delete Branch| [Delete](manage-branches.html#delete-branch) the selected branch  
![the Show diff icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.vcs.diff.svg)| Compare with Current| [Compare](manage-branches.html#compare_branches) the selected branch with the branch that is currently checked out.  
![the Search icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.search.svg)| Show My Branches| Filter the list to only display branches created by you.  
![the Fetch button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.vcs.fetch.svg)| Fetch All Remotes| [Fetch](sync-with-a-remote-repository.html#fetch) changes from all remote branches.  
![the Star icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.nodes.star.svg)| Mark/Unmark as Favorite| Mark the selected branch as a favorite one. Favorite branches are displayed on top of the list.   
![the Group By Directory icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.actions.groupByPackage.svg)| Group By Directory| Group the branches by directory.  
![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.expandAll.svg) ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.collapseAll.svg)| Expand All / Collapse All| Expand/collapse the list  
  
### Branches pane context menu

Item| Description  
---|---  
Checkout| [Checkout](manage-branches.html#switch-branches) the selected branch.  
New Branch From Selected| [Create a new branch based on the selected branch](manage-branches.html#create-branch-from-selected).  
Checkout and Rebase onto Current| [Rebase](apply-changes-from-one-branch-to-another.html#rebase-branch) a branch on top of the current branch.  
Compare with Current| [Compare](manage-branches.html#compare_branches) the selected branch with the branch that is currently checked out.  
Show Diff with Working Tree| Compare the selected branch with the local state of the branch that is currently checked out.   
Rebase Current onto Selected| [Rebase](apply-changes-from-one-branch-to-another.html#rebase-branch) the current branch on top of the selected one. This is equivalent to running `git rebase` with the selected branch name.  
Pull into Current Using Rebase| Fetch changes from the selected branch and [rebase](apply-changes-from-one-branch-to-another.html#rebase_branch_on_top_of_another_branch) the current branch on top of these changes.  
Pull into Current Using Merge| Fetch changes from the selected branch and [merge](apply-changes-from-one-branch-to-another.html#merge) them into the current branch.  
Update| [Pull](sync-with-a-remote-repository.html#pull) changes from the selected branch. You can select multiple branches to update them in a batch.  
Push| [Push](commit-and-push-changes.html#push) outgoing commits to the selected branch.  
Rename| Rename the selected branch.  
Delete| [Delete](manage-branches.html#delete-branch) the selected branch. You can select multiple branches to delete them in a batch.
