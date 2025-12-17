[//]: # (Source: https://www.jetbrains.com/help/idea/managing-mercurial-branches-and-bookmarks.html)
[//]: # (Downloaded: 2025-12-17 19:31:52)

## Branches

### Create a named branch

The new branch immediately becomes active and its name is shown on the Mercurial Branches widget in the Status bar.

  1. Click the Mercurial Branches widget in the status bar to open the Branches popup and click New Branch.

  2. In the Create New Branch dialog that opens, specify the name of the new branch.




### Close a branch

According to [Mercurial workflows](https://www.mercurial-scm.org/wiki/Workflows), when you are done with a feature development and do not expect any further changes, you close the corresponding branch. A closed branch is not displayed among active branches, in the [Log view](log-tab.html), and so on. To close a branch, do the following:

  1. Click the Mercurial Branches widget in the status bar to open the Branches popup and click Close Branch.

  2. In the Branches popup, click Close branch. The Commit changes dialog will be displayed.

  3. Click Commit and Close. All changes will be committed and the current branch will be closed.




Note that if you have several repositories listed in the Repositories section, the corresponding menu option will toggle to Close Branches and the `close` operation will be applied to all of them.
