[//]: # (Source: https://www.jetbrains.com/help/idea/switching-between-working-directories.html)
[//]: # (Downloaded: 2025-12-17 20:03:45)

# Switch between Mercurial working directories

The Mercurial integration with IntelliJ IDEA provides the possibility to switch update the repository's [working directory](https://www.mercurial-scm.org/wiki/WorkingDirectory) to the specified [changeset](https://www.mercurial-scm.org/wiki/UnderstandingMercurial#Revisions.2C_changesets.2C_heads.2C_and_tip) or a specific [line of development](https://www.mercurial-scm.org/wiki/Branch). Changesets can be identified by their hashes or by previously assigned [tag identifiers](https://www.mercurial-scm.org/wiki/Tag).

By default, Mercurial requires that before update the current working directory should be clean. If your current working copy is not clean, you can either commit the changes or shelve them as described in [Shelve or stash changes](shelving-and-unshelving-changes.html).

### Quickly switch to another branch or bookmark

  1. In the Status bar, click the Mercurial Branch widget to open the Branches popup.

  2. Select the branch or bookmark to which you want to switch and in the menu that opens, click Update. 

![Mercurial widget in Status bar](https://resources.jetbrains.com/help/img/idea/2025.3/mercurialSwitchBranch.png)



### Switch to another working directory

  1. In the main menu, go to Hg | Mercurial | Update to.

  2. In the Switch Working Directory dialog that opens, specify the target working directory:

     * To switch to another line of development, choose Branch and select the desired branch from the list.

     * To switch to a changeset to which you have previously assigned a tag identifier, choose Tag and select the desired tag from the drop-down list.

     * To switch to a changeset identified by a hash, choose Revision and type the desired revision number in the field.

![Switching to another working directory](https://resources.jetbrains.com/help/img/idea/2025.3/mercurialSwitchDirectory.png)
  3. To have any local changes overwritten, select the Overwrite locally modified files (no backup) checkbox.

  4. As soon as a conflict takes place, the Conflicts dialog opens with a list of conflicting files to resolve.




23 February 2024

[Tag changesets and repositories](tagging-changesets.html)[Pull changes from the Mercurial upstream (Pull)](updating-a-local-mercurial-repository-pull.html)
