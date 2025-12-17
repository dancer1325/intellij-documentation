[//]: # (Source: https://www.jetbrains.com/help/idea/manage-branches.html)
[//]: # (Downloaded: 2025-12-17 19:31:44)

## Create a new branch

### Create a new branch from the current branch

  1. In the Branches popup, choose New Branch or right-click the current branch in the Branches pane of the Git tool window and choose New Branch from 'branch name'.

  2. In the dialog that opens, specify the branch name, and make sure the Checkout branch option is selected if you want to switch to that branch.

Once you start typing a name for your new branch, IntelliJ IDEA will suggest relevant prefixes based on the names of existing local branches.

The new branch will start from the current branch HEAD.




### Create a new branch from the selected branch

  1. In the Branches popup or in the Branches pane of the Git tool window select a local or a remote branch that you want to start a new branch from and choose New Branch from Selected.

  2. In the dialog that opens, specify the branch name, and make sure the Checkout branch option is selected if you want to switch to that branch.




### Create a new branch from the selected commit

  1. In the [Log view](log-tab.html), select the commit that you want to act as a starting point for the new branch and choose New Branch from the context menu.

![New branch from a selected commit in the Log tab](https://resources.jetbrains.com/help/img/idea/2025.3/branch_from_commit.png)
  2. In the dialog that opens, specify the branch name, and make sure the Checkout branch option is selected if you want to switch to that branch.



