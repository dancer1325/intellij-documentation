[//]: # (Source: https://www.jetbrains.com/help/idea/uploading-a-local-mercurial-repository-push.html)
[//]: # (Downloaded: 2025-12-17 20:05:11)

## Force push

When you run `push`, Mercurial will refuse to complete the operation if the remote repository has changes that you are missing and that you are going to overwrite with your local copy of the repository. Normally, you need to perform `pull` to synchronize with the remote before you update it with your changes.

The `--force push` command disables this check and lets you overwrite the remote repository, thus erasing its history and causing data loss.

A possible situation when you may still need to perform `--force push` is when you rebase a pushed branch and then want to push it to the remote server. In this case, when you try to push, Mercurial will reject your changes because the remote ref is not an ancestor of the local ref. If you perform `pull` in this situation, you will end up with two copies of the branch which you then need to merge.

Rebasing a pushed branch and modifying its history should be avoided unless absolutely necessary (for example, if you've accidentally pushed some sensitive data).

Using the `--force` will lead to all new heads being pushed on all branches, which is likely to cause confusion for your team.

If you decide to force push the rebased branch and you are working in a team, make sure that:

  * Nobody has pulled your branch and done some local changes to it

  * All pending changes have been committed and pushed

  * You have the latest changes for that branch



