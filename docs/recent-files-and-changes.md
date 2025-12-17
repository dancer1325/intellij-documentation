[//]: # (Source: https://www.jetbrains.com/help/idea/recent-files-and-changes.html)
[//]: # (Downloaded: 2025-12-17 19:56:53)

# Recent files and changes

When working on a project, you often need to switch between files and locations you've recently viewed or edited. IntelliJ IDEA provides quick navigation features that help you find and reopen recent files or revisit edited code fragments.

### Find recent files

You can search for recently opened or edited files using the Recent Files popup.

  * To open the Recent Files popup, press `Ctrl+E`.

![Recent files](https://resources.jetbrains.com/help/img/idea/2025.3/recent_files.png)
  * To show only recently edited files, press `Ctrl+E` again or select the Show edited only option.

  * To search for items within the popup, start typing your search query. IntelliJ IDEA filters the results dynamically as you type, showing only the matching items.

![Recent files search](https://resources.jetbrains.com/help/img/idea/2025.3/recent_files_search.png)



### Find recent locations

You can check your recently viewed or changed code using the Recent Locations popup.

  * To open the Recent Locations popup, press `Ctrl+Shift+E`. The list starts with the latest visited location at the top and contains code snippets.

![Recent Locations popup](https://resources.jetbrains.com/help/img/idea/2025.3/recent_locations_popup.png)
  * To show only the locations with changed code, while in the popup, use the `Ctrl+Shift+E` shortcut again or select the Show edited only option.

![Show changed only option](https://resources.jetbrains.com/help/img/idea/2025.3/only_changed_code_locations.png)
  * To search for a code snippet, in the Recent Locations popup, start typing your search query. You can search by the code text, file name, or [breadcrumbs](using-code-editor.html#breadcrumbs).

![Search locations](https://resources.jetbrains.com/help/img/idea/2025.3/search_locations.png)
  * To delete a location entry from the search results, press either `Delete` or `Backspace`.

Keep in mind that the deleted location is also removed from the list of entries that you [access with the `Ctrl+Alt+Left` shortcut](navigating-through-the-source-code.html#back_forward).




### Find recent changes

You can use the Recent Changes list to get a list of recent changes made locally or externally in your project. If necessary, you can revert those changes.

  1. In the main menu, go to View | Recent Changes `Alt+Shift+C`. 

![the Recent Changes popup](https://resources.jetbrains.com/help/img/idea/2025.3/recent_changes.png)
  2. In the Recent Changes tab of the [Local History](local-history.html) tool window, select a change.

The IDE shows you a list of files modified with this change in the panel below.

  3. Press `Enter` or double-click the file to open the diff viewer where you can check what was changed and revert those changes if necessary.




### Navigate between changes

If you edit a file that is [under version control](enabling-version-control.html), IntelliJ IDEA provides several ways to move back and forth with the updates. In particular, you can use the navigation commands, keyboard shortcuts, and the change markers.

  * Press `Ctrl+Alt+Shift+Down`/`Ctrl+Alt+Shift+Up`.

  * In the main menu, go to Navigate | Next / Previous Change.

  * Click a [change marker](adding-files-to-version-control.html#track_changes), and then click ![the Previous Change button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.up.svg) or ![the Next Change button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.down.svg).

  * To navigate to the place of your last edit, press `Ctrl+Shift+Backspace` or select Navigate | Last Edit Location from the main menu.




14 September 2025

[File navigation](file-navigation.html)[Source code hierarchy](viewing-structure-and-hierarchy-of-the-source-code.html)
