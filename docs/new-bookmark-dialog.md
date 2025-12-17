[//]: # (Source: https://www.jetbrains.com/help/idea/new-bookmark-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:32:59)

# New Bookmark dialog

Use this dialog to establish a new light-weight Mercurial branch (bookmark). The bookmark will immediately appear in the Branches popup. You can create both active and inactive bookmarks. By default, IntelliJ IDEA creates an active bookmark, so you are immediately switched to the new bookmark, and it is marked with a tick in the Branches popup. If you do not want to move your development to the new bookmark right now, you can create an inactive bookmark and switch to it later. Note that tracking and updating is available only for the bookmark that is currently active. You can have only one active bookmark. For more information, refer to [Bookmarks](https://www.mercurial-scm.org/wiki/Bookmarks) and [Manage Mercurial branches and bookmarks](managing-mercurial-branches-and-bookmarks.html).

Item| Description  
---|---  
Bookmark Name| In this field, type the name of the bookmark. This identifier will always point at the head of the new light-weight branch as you commit changes. You can use this name to identify the head of the relevant light-weight branch when during update or merge.  
Inactive| 

  * Clear this checkbox to activate the new bookmark and thus enable tracking and updating the light-weight branch the bookmarks identifies. The checkbox is cleared by default.
  * Select this checkbox to have an inactive bookmark created, that is, to remain in the current light-weight branch (bookmark) or named branch and switch to the new bookmark later.

  
  
11 February 2024

[Merge dialog (Mercurial)](merge-dialog-mercurial.html)[Pull dialog](pull-dialog.html)
