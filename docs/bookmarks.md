[//]: # (Source: https://www.jetbrains.com/help/idea/bookmarks.html)
[//]: # (Downloaded: 2025-12-17 19:19:27)

## Add bookmarks

IntelliJ IDEA adds your bookmarks to the predefined list in the Bookmarks tool window that is created automatically and has the same name as the project. You can [create more lists](#create-list) and [set another list as default](#change-default-list).

### Add an anonymous line bookmark

  * In the editor, place the caret at a line of code and press `F11`.

  * Alternatively, right-click the gutter next to the line of code that you want to bookmark and select Add Bookmark. 

![Anonymous bookmark placed in the gutter](https://resources.jetbrains.com/help/img/idea/2025.3/ij-anonymous-bookmark.png)



A bookmark icon appears in the gutter next to the bookmarked line.

### Add a mnemonic line bookmark

  1. In the editor, place the caret at a line of code and press `Ctrl+F11`.

Alternatively, right-click the gutter next to the line of code that you want to bookmark and select Add Mnemonic Bookmark.

  2. In the popup that opens, select a number or a letter that you want to use as an identifier for this bookmark.

![Adding a mnemonic bookmark](https://resources.jetbrains.com/help/img/idea/2025.3/ij-add-mnemonic.png)

If the selected mnemonic is already used, the IDE will ask you whether you want to overwrite an existing bookmark with the new one. Select the Don't ask again option to silently overwrite mnemonics.

  3. Optionally, provide a description for the new bookmark.

  4. Press `Enter` or click the selected letter or number once again to save the bookmark.

A letter or a number bookmark icon appears in the gutter next to the bookmarked line.




If you want to bring back the confirmation dialog that is shown before replacing an existing mnemonic with a new one, click ![Show Options Menu](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.moreVertical.png) in the Bookmarks tool window and enable the Ask Before Rewriting Mnemonic option.

To take a look at all line bookmarks that you have in code, press `Shift+F11` or go to Edit | Bookmarks | Show Line Bookmarks in the main menu.

### Bookmark files, packages, folders, and modules

  1. In the Project tool window `Alt+1`, right-click an item that you want to bookmark and select Bookmarks | Add Bookmark (`F11`) or Add Mnemonic Bookmark (`Ctrl+F11`).

To bookmark multiple items, select them in the tool window, right-click one of them, and select Bookmarks | Add Bookmarks (`F11`).

  2. For mnemonic bookmarks, select a number or a letter that you want to use as an identifier for this bookmark.

Press `Enter` or click the selected letter or number once again to save the bookmark.




### Bookmark an editor tab

You can bookmark files from editor tabs one by one. These bookmarks will be added to the [default list](#change-default-list).

  1. Right-click the tab with the file that you want to bookmark and select Bookmarks | Add Bookmark (`F11`) to add an anonymous bookmark or Add Mnemonic Bookmark (`Ctrl+F11`) to add a bookmark with an identifier.

  2. For mnemonic bookmarks, select a number or a letter that you want to use as an identifier for this bookmark.

Press `Enter` or click the selected letter or number once again to save the bookmark.




### Bookmark all editor tabs

You can quickly bookmark all open files and add these bookmarks to the new list.

  1. Click the Recent Files, Tab Actions, and More icon ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moreVertical.svg) that is on the tab bar and select Bookmark Open Tabs. 

  2. Name the new list.

You can use this list for new bookmarks [by default](#change-default-list): enable the Use as default list option.

The IDE will create a new list and add to this list all files from the open tabs.

![Bookmark editor tabs](https://resources.jetbrains.com/help/img/idea/2025.3/ij_bookmark_all_editor_tabs.png)


