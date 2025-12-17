[//]: # (Source: https://www.jetbrains.com/help/idea/apply-changes-from-one-branch-to-another.html)
[//]: # (Downloaded: 2025-12-17 19:18:28)

## Merge branches

Suppose you have created a feature branch to work on a specific task, and want to integrate the results of your work (`F1`, `F2`, `F3`) into the main code base after you have completed and tested your feature:

mainfeatureC1C2C3F1F2F3

Merging your branch into `main` is the most common way to do this.

It is very common that while you are working in your feature branch, your teammates continue to commit their work (`C4`, `C5`) to `main`:

mainfeatureC1C2C3F1F2F3C4C5

When you [merge](#merge-branches) your feature branch into `main`, the changes from your feature branch are integrated into the HEAD of the target branch:

mainfeatureC1C2C3F1F2F3C4C5

Git creates a new commit that is referred to as a merge commit that results from combining the changes from your feature branch and `main` from the point where the two branches diverged.

The major benefit of merging is full traceability, as commits merged into the `main` code base preserve their original hash and author, and all commits that are part of one feature can be grouped together.

This workflow is good for projects where committing changes to the `main` code base involves [pull](create-and-merge-github-pull-requests.html#create-pull-request) or [merge requests](work-with-gitlab-merge-requests.html), or a hierarchical approval procedure, as existing branches are not changed in any way.

The main drawback of this approach is that extraneous merge commits are created each time you need to incorporate changes, which intensely pollutes project history and makes it difficult to read.

### Merge branches

  1. In the [Branches](manage-branches.html) popup (main menu Git | Branches) or in the Branches pane of the Git tool window, select the target branch that you want to integrate the changes to, and choose Checkout from the context menu to switch to that branch.

  2. Do one of the following:

     * If you do not need to specify options for the merge, select the branch that you want to merge into the current branch and choose Merge <branch_name> into <target_branch> from the submenu.

![Merge branches](https://resources.jetbrains.com/help/img/idea/2025.3/merge_branches_popup.png)
     * If you need to specify merge options, from the main menu choose Git | Merge to open the Merge dialog:

![The Merge dialog](https://resources.jetbrains.com/help/img/idea/2025.3/merge_dialog.png)

Select the branch that you want to merge into the current branch, click Modify options and choose from the following:

       * `--no-ff`: a merge commit will be created in all cases, even if the merge could be resolved as a fast-forward.

       * `--ff-only`: the merge will be resolved only if it is possible to fast-forward.

       * `--squash`: a single commit with all pulled changes will be created on top of the current branch.

       * `-m`: you will be able to edit the message for the merge commit.

       * `--no-commit`: a merge will be performed, but a merge commit will not be created so that you can inspect the result of the merge before committing.

       * `--no-verify`: performs the merge while bypassing the pre-merge and commit-message hooks that normally run by default.

       * `--allow-unrelated-histories`: performs a merge, overriding the safety rule that refuses to merge histories without a common ancestor.

Click Merge.




If your working tree is clean (which means you have no uncommitted changes), and no conflicts occur between your feature branch and the target branch, Git will merge the two branches, and the merge commit will appear in the Log tab of the Git tool window `Alt+9`:

![merge commit](https://resources.jetbrains.com/help/img/idea/2025.3/merge_commit.png)

If conflicts occur between your branch and the target branch, you will be prompted to resolve them (refer to [Resolve conflicts](resolve-conflicts.html)). If there are unresolved conflicts left after a merge, the Merge Conflicts node will appear in the corresponding changelist in the Commit tool window `Alt+0` with a link to resolve them.

If you have local changes that will be overwritten by merge, IntelliJ IDEA will suggest performing Smart merge. If you select this option, IntelliJ IDEA will [stash](shelving-and-unshelving-changes.html#stash) uncommitted changes, perform merge, and then unstash the changes.

You can cancel an unfinished merge operation by selecting the Abort action from the Git Branches popup.
