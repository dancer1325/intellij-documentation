[//]: # (Source: https://www.jetbrains.com/help/idea/use-tags-to-mark-specific-commits.html)
[//]: # (Downloaded: 2025-12-17 20:05:15)

# Use tags to mark specific Git commits

Git allows you to attach tags to commits to mark certain points in the project history so that you can refer to them in the future. For example, you can tag a commit that corresponds to a release version, instead of [creating a branch](manage-branches.html#create-branch) to capture a release snapshot.

In IntelliJ IDEA, you can perform operations with tags in the Git Branches popup. To invoke it, in the main window header, click the Git widget with the name of the branch that is currently checked out:

![Tags node in the branches popup](https://resources.jetbrains.com/help/img/idea/2025.3/tags_in_branches_popup.png)

You can also manage tags in the [Branches pane](log-tab.html#BranchesPane) of the Git tool window `Alt+9`.

![Branches pane](https://resources.jetbrains.com/help/img/idea/2025.3/branches_pane.png)

### Assign a tag to a commit

  1. Open the Git tool window `Alt+9` and switch to the Log tab.

  2. Locate the commit you want, right-click it and select New Tag from the context menu.

  3. Enter the name of the new tag and click OK. The tag will be shown in the Log tab of the Git tool window `Alt+9`:

![Tagged commit](https://resources.jetbrains.com/help/img/idea/2025.3/tagged_commit.png)



### Assign an annotated tag to a commit

Meta-data for annotated tags contains the name of the user who created them, so they allow you to check who placed them.

  1. In the main menu, go to Git | New Tag.

  2. In the Tag dialog that opens, under Git Root, select the path to the local repository in which you want to tag a commit, and specify the name of the new tag.

  3. In the Commit field, specify the commit that you want to tag. You can enter the commit hash, or use an expression, for example: `<branch>~<number of commits backwards between the latest commit (HEAD) and the required commit>`. For more information, refer to Git [commit naming](http://www.kernel.org/pub/software/scm/git/docs/user-manual.html#naming-commits) conventions.

  4. Enter some comment in the Message field to create an annotated tag (if it's empty, a regular tag will be created).

  5. Click Create Tag.




If the Compact References View option is enabled under Quick Settings in the Log toolbar, tag names are hidden behind branch names and are not visible.

You can also right-click a commit in the Log tab of the Version Control tool window `Alt+9` and select New Tag from the context menu if you do not need to specify any additional options.

### Reassign an existing tag

If you've placed a tag on a wrong commit, and want to reassign it (for example, to indicate a commit for a release version), do the following:

  1. In the main menu, go to Git | New Tag.

  2. In the Tag dialog, in the Tag Name field specify the name of an already existing tag that you want to reassign.

  3. Select the Force option.

  4. In the Commit field, specify the commit where to move the tag and click Create Tag.




### Jump to a tagged commit

  1. Open the Git tool window `Alt+9` and switch to the Log tab.

  2. Click the Go To Hash/Branch/Tag icon ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.toolwindow.find.svg) on the toolbar, or press `Ctrl+F`. 

![Go to Hash/Branch/Tag icon](https://resources.jetbrains.com/help/img/idea/2025.3/go_to_hash.png)
  3. Enter the tag name ([code completion](auto-completing-code.html) suggests tag names as you type) and press `Enter`.




### Check out a tagged commit

Suppose you marked a commit that corresponds to a release version with a tag, and now you want to review the snapshot of your project at that point in time. You can do this by checking out a tagged commit. Do one of the following:

  * [Locate](#jump-to-tag) the tagged commit that you want to checkout, right-click it and select Checkout Revision from the context menu.

  * In the Git tool window `Alt+9`, open the Tags node, select the necessary tag and choose Checkout from the list of actions in the context menu.

  * [Invoke the branches popup](manage-branches.html#invoke-branches-popup), click Checkout Tag or Revision and type in the tag name (IntelliJ IDEA provides a list of matching tags and revisions as you type).

  * [Invoke the branches popup](manage-branches.html#invoke-branches-popup), open the Tags node, select the necessary tag and choose Checkout from the list of actions in the context menu.




Note that this operation results in a [detached HEAD](https://git-scm.com/docs/git-checkout#_detached_head), which means you are no longer in any branch. You can use this snapshot for inspection and experiments. However, if you want to commit changes on top of this snapshot, you will need to [create a branch](manage-branches.html#create-branch).

### Fetch tags

You can set the way Git fetches tags when you [fetch changes](sync-with-a-remote-repository.html#fetch) from the upstream.

  1. Press `Ctrl+Alt+S` to open settings and then select Version Control | Git | Fetch tags.

  2. Select the preferred option:

     * Auto: follow the fetch rules specified in the config file.

For example, you can specify different fetch rules for different remotes. Check the [git fetch](https://git-scm.com/docs/git-fetch) documentation for possible options.

If no fetch rules are specified, then by default, Git fetches only tags that point at commits that are downloaded from the remote repository.

     * Sync: when fetching updates, remove any local tags that no longer exist on the remote (same as `git fetch --prune-tags`).

     * Always: always fetch all tags from the remote when fetching updates (same as `git fetch --tags`).

     * Never: do not fetch tags that point at commits that are downloaded from the remote repository (same as `git fetch --no-tags`).




### Push a tag

By default, when you perform the `push` operation, tags are not sent to the remote repositories.

To push a particular tag, either invoke [the branches popup](manage-branches.html#invoke-branches-popup) or the Git tool window `Alt+9`, open the Tags node, select the necessary tag and choose Push to origin from the list of actions in the context menu.

To push several tags together with the commits:

  1. In the Push Commits dialogue, select the Push tags checkbox in the bottom-left corner. 

![Push Tags option in the Push Commits dialogue](https://resources.jetbrains.com/help/img/idea/2025.3/push_tags.png)
  2. In the drop-down menu, select the tags you want to push:

     * Select All if you want to push all tags, including the tags that do not belong to the selected branches you are about to push (equivalent to `push --tags`).

     * Select Current Branch if you want to push only the tags that belong to the selected branches you are about to push (equivalent to `push --follow-tags`).

  3. Click Push.




### Delete a tag

  * [Locate](#jump-to-tag) a tagged commit, right-click it and select Tag <tag_name> | Delete from the context menu.

  * In the Git tool window `Alt+9`, open the Tags node, select the necessary tag and choose Delete from the list of actions in the context menu.

  * [Invoke the branches popup](manage-branches.html#invoke-branches-popup), open the Tags node, select the necessary tag and choose Delete from the list of actions in the context menu.




11 July 2025

[Undo changes in Git repository](undo-changes.html)[Edit Git project history](edit-project-history.html)
