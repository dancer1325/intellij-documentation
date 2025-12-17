[//]: # (Source: https://www.jetbrains.com/help/idea/finding-and-replacing-text-in-project.html)
[//]: # (Downloaded: 2025-12-17 19:27:09)

# Search and replace a target within a project

You can search for a text string within a project, use different scopes to narrow your search process, find occurrences, and exclude certain items from the search. 

### Find the search string in a project

  1. Press `Ctrl+Shift+F` or select Edit | Find | Find in Files from the main menu.

  2. In the search field, type your search string. Alternatively, in the editor, highlight the string you want to find and press `Ctrl+Shift+F` or from the context menu, select Find in Files. IntelliJ IDEA places the highlighted string into the search field.

To see a list of your previous searches, press `Alt+Down`.

If you need, specify the additional options.

![Find in Files](https://resources.jetbrains.com/help/img/idea/2025.3/find_in_path.png)

IntelliJ IDEA lists the search strings and the files that contain them. If the search string is found several times on the same line of code, IntelliJ IDEA merges the results in one line.

To do a multi-line search, click the ![Multi-line search](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.searchNewLineHover.svg) icon to enter a new line, and press `Ctrl+Alt+Down`/`Ctrl+Alt+Up` to browse through occurrences.

  3. Check the results in the preview area of the dialog where you can replace the search string or select another string, press `Ctrl+Shift+F` again and start a new search.

  4. To see the list of occurrences in a separate tool window, click Open in Find Window. Use this window and its options to group the results, preview them, and work with them further.

If you want to see each new search result in a separate tab in the Find tool window, select the Open Results in New Tab checkbox on the bottom of the Find in Files dialog.




### Copy paths or references of the found files

  1. In the list of search results, right-click the result for which you want to copy a path and click Copy/Reference.

![Copy/Reference](https://resources.jetbrains.com/help/img/idea/2025.3/copy_path_reference.png)
  2. In the Copy window, select the path or reference you need.

![the Copy window](https://resources.jetbrains.com/help/img/idea/2025.3/copy_window.png)



### Narrow your search

You can use different options in the Find in Files dialog to adjust your search process.

  * Select options such as Words (![the Words icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.inline.exactWords.svg)) or Match case (![the Match case icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.inline.matchCase.svg)) to find the exact word in a project or match the letter case.

  * With ![the Regex icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.regex.svg) selected, IntelliJ IDEA automatically escapes special regex symbols with backslash `\` when you search for a text string that contains them.

Keep in mind that if you copy (`Ctrl+C`) the string first and then paste (`Ctrl+V`) it in the search field, the regex symbols will not be taken into account.

For more information about regex, refer to the [search with regex](tutorial-finding-and-replacing-text-using-regular-expressions.html) documentation.

  * Click the ![filter](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.filter.svg) icon to filter your search. For example, you can filter the search to omit comments or search only in comments instead.

  * Select one of the displayed options such as Module or Directory to limit your search. 

Moreover, you can select the Scope option that offers you a list of [predefined scopes](configuring-scopes-and-file-colors.html#predefined-scopes-list) for your search. For example, you can limit your search only to the open files in your project or you can search in a class hierarchy. 

![Search in class hierarchy](https://resources.jetbrains.com/help/img/idea/2025.3/class_hierarchy.png)

If you work without tabs, the scope Recently Viewed Files or Recently Changed Files option might become useful. You can also create your own custom scope, click the Browse icon (![ellipsis icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg)) to open the [Scopes](configuring-scopes-and-file-colors.html) dialog.




### Search in the specific file types

Use the File mask option to narrow your search to a specific file type. You can select the existing file type from the list, add a new file type, or add an additional file mask syntax to search for file types with certain patterns.

  1. In the Find in Files dialog, select the File mask checkbox and from the list of file types, select the one you need.

![File mask](https://resources.jetbrains.com/help/img/idea/2025.3/file_mask_search.png)

IntelliJ IDEA limits its search to the specified type.

  2. If you don't find the file type you need in the list, enter your file type in the File mask field.

For example, use the following syntax to search only in gradle files: *.gradle.

You can manually add a file mask in the search field. If necessary, specify several file types separating them with commas.

![Add a new file type](https://resources.jetbrains.com/help/img/idea/2025.3/add_new_file_type.png)



### Replace the search string in a project

  1. Press `Ctrl+Shift+R` to open the Replace in Path dialog.

  2. In the top field, enter your search string. In the bottom field, enter your replacement string.

![Replace in path dialog](https://resources.jetbrains.com/help/img/idea/2025.3/Replace_in_path_dialog.png)

For example, if you want to replace a variable name with a new name for a large project, use the Replace in path instead of the Rename refactoring since your variable can appear in the config files as well.

  3. Click one of the available Replace commands.




### Work with the search results in the Find tool window

  1. In the Find in Files dialog, click Open in Find Window to open the list of the search results in a separate window.

  2. Using icons and context menu in the Find tool window, you can sort entries, exclude directories, navigate to the source code, and so on.

![the Find tool window](https://resources.jetbrains.com/help/img/idea/2025.3/find_tool_window.png)

Check the following popular options:

     * If you want to exclude a directory from the results, select a directory and from the context menu, select Exclude.

     * To locate the result of the search in the editor, use the Jump to Source option from the context menu.

     * To return back to the Find in Files dialog, click ![the Settings icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) on the left toolbar.

     * To sort the search entries, select View Options | Sort Members Alphabetically in Show Options Menu (![the Show Options Menu](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg)).

For more information about the options and icon references of the Find tool window, refer to the [Find tool window](find-tool-window.html) reference section.




16 December 2024

[Search for a target within a file](finding-and-replacing-text-in-file.html)[Find and replace text using regular expressions](tutorial-finding-and-replacing-text-using-regular-expressions.html)
