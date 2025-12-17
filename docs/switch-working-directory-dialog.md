[//]: # (Source: https://www.jetbrains.com/help/idea/switch-working-directory-dialog.html)
[//]: # (Downloaded: 2025-12-17 20:03:43)

# Switch Working Directory dialog

Use this dialog to update the [current working directory](https://www.mercurial-scm.org/wiki/WorkingDirectory) to a [named branch](https://www.mercurial-scm.org/wiki/Branch), [light-weight branch (bookmark)](https://www.mercurial-scm.org/wiki/Bookmarks), or a specific [changeset](https://www.mercurial-scm.org/wiki/ChangeSet) identified by a tag, hash, or revision number. 

By default, Mercurial requires that before update the current working directory should be clean, that is, it should not contain any uncommitted changes. Otherwise the update operation fails and IntelliJ IDEA shows the corresponding error message. The message also recommends that you clean the current working directory by running the `hg update <target branch, bookmark, or changeset> -C` to discard the uncommitted changes. 

Item| Description  
---|---  
Repository| From this list, choose the repository to run the update in. The contents of the Branch, Tag, and Bookmark lists are updated to show the branches, tags, and bookmarks that are available in the selected repository.   
Switch to| In this area, choose the branch, bookmark, or changeset to switch to. 

  * Branch: choose this option to switch to another line of development identified by a [branch name](https://www.mercurial-scm.org/wiki/Branch) and update to the [branch head](https://www.mercurial-scm.org/wiki/Head). Choose the desired branch from the list which shows all the named branches available in the current repository. 
  * Tag: choose this option to update to a [changeset](https://www.mercurial-scm.org/wiki/ChangeSet) to which you have previously assigned a [tag identifier](https://www.mercurial-scm.org/wiki/Tag). Choose the relevant tag from the list. The list shows both local tags (from .hg/localtags) and global tags (from .hgtags).
  * Bookmark: choose this option to switch to another line of development which is identified by a [bookmark](https://www.mercurial-scm.org/wiki/Bookmarks) and update to its head. Choose the relevant bookmark from the list which shows all the available light-weight branches in the current repository. 
  * Revision: choose this option to update to a specific changeset identified by its hash or revision number. In the field, type the relevant revision number or paste the hash. To copy a hash, open the Log tab of the Version Control tool window `Alt+9`, select the relevant branch and revision, and then choose Copy Hash from the context menu of the selection. 

  
Overwrite locally modified files (no backup)| If you are going to update to another branch, bookmark, or changeset and you have any uncommitted changes in the current line of development, technically there can be two ways to treat them. The uncommitted changes can be either committed before update or abandoned (cleaned). By default, Mercurial requires that before update the current working directory should be clean, that is, it should not contain any uncommitted changes. Otherwise the update operation fails and IntelliJ IDEA shows the corresponding error message. The message also recommends that you clean the current working directory by running the `hg update <target branch, bookmark, or changeset> -C` to discard the uncommitted changes. Use the Overwrite locally modified files (no backup) checkbox to prevent failures during update when the current working copy is not clean.

  * Select the checkbox to abandon any uncommitted local changes.
  * Clear the checkbox if you are sure that the current working directory is clean.

  
  
11 February 2024

[Pull dialog](pull-dialog.html)[Tag dialog (Mercurial)](tag-dialog-mercurial.html)
