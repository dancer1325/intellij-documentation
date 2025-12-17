[//]: # (Source: https://www.jetbrains.com/help/idea/merge-dialog-mercurial.html)
[//]: # (Downloaded: 2025-12-17 19:32:20)

# Merge dialog (Mercurial)

Use this dialog to merge the [current working directory](https://www.mercurial-scm.org/wiki/WorkingDirectory) to a [named branch](https://www.mercurial-scm.org/wiki/Branch), [light-weight branch (bookmark)](https://www.mercurial-scm.org/wiki/Bookmarks), or a specific [changeset](https://www.mercurial-scm.org/wiki/ChangeSet) identified by a tag, hash, or revision number. 

By default, Mercurial requires that before merge the current working directory should be clean, that is, it should not contain any uncommitted changes. Otherwise the merge operation fails and IntelliJ IDEA shows the corresponding error message. The message also recommends that you clean the current working directory by running the `hg merge <target branch, bookmark, or changeset> -C` to discard the uncommitted changes. 

Item| Description  
---|---  
Repository| From this list, choose the repository to run the merge in. The contents of the Branch, Tag, and Bookmark lists are updated to show the branches, tags, and bookmarks that are available in the selected repository.   
Merge with| In this area, choose the branch, bookmark, or changeset to merge with. 

  * Branch: choose this option to switch to another line of development identified by a [branch name](https://www.mercurial-scm.org/wiki/Branch) and merge to the [branch head](https://www.mercurial-scm.org/wiki/Head). Choose the desired branch from the list which shows all the named branches available in the current repository. 
  * Tag: choose this option to merge to a [changeset](https://www.mercurial-scm.org/wiki/ChangeSet) to which you have previously assigned a [tag identifier](https://www.mercurial-scm.org/wiki/Tag). Choose the relevant tag from the list. The list shows both local tags (from .hg/localtags) and global tags (from .hgtags).
  * Bookmark: choose this option to switch to another line of development which is identified by a [bookmark](https://www.mercurial-scm.org/wiki/Bookmarks) and merge to its head. Choose the relevant bookmark from the list which shows all the available light-weight branches in the current repository. 
  * Revision: choose this option to merge to a specific changeset identified by its hash or revision number. In the field, type the relevant revision number or paste the hash. To copy a hash, open the Log tab of the Version Control tool window `Alt+9`, select the relevant branch and revision, and then choose Copy Hash from the context menu of the selection. 

  
  
11 February 2024

[Create Mercurial Repository dialog](create-mercurial-repository-dialog.html)[New Bookmark dialog](new-bookmark-dialog.html)
