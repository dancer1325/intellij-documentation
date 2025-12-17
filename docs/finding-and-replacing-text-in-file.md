[//]: # (Source: https://www.jetbrains.com/help/idea/finding-and-replacing-text-in-file.html)
[//]: # (Downloaded: 2025-12-17 19:27:08)

# Search for a target within a file

You can quickly find and replace text strings in the current document. Using different options, you can narrow your search process, use [regular expressions](tutorial-finding-and-replacing-text-using-regular-expressions.html) in your search, and manage your search results.

### Find the search string in a file

  1. Open your file in the editor.

  2. Press `Ctrl+F` or select Edit | Find | Find from the main menu.

If you want to extend the search of your target beyond the current file, press `Ctrl+Shift+F`. For more information, refer to [Search and replace a target within a project](finding-and-replacing-text-in-project.html). 

  3. In the search field that opens, enter your search string. IntelliJ IDEA highlights the results of your search in the file. Alternatively, in the editor, highlight the string you want to find and press `Ctrl+F`. IntelliJ IDEA places the highlighted string into the search field. 

![Search string](https://resources.jetbrains.com/help/img/idea/2025.3/search_within_a_file.png)

Place the caret at any string in your file and press `Ctrl+F` to find its occurrences or go to Edit | Find | Next Occurrence of the Word at Caret in the main menu. 




### Find in selection

You can search for a text string inside a multi-line selection.

IntelliJ IDEA handles replacing in multi-line selections the same way.

  1. Select a multi-line fragment and press `Ctrl+F`. 

  2. Click ![the Filter Search Results icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.filter.svg), set a tick next to Search In Selection and type your search string. IntelliJ IDEA will search for the target inside the selected fragment first.

If you remove the tick next to Search In Selection, IntelliJ IDEA will switch the search process back to the whole file.

![Find in selection](https://resources.jetbrains.com/help/img/idea/2025.3/find_in_selection.png)

If you want to search for the multi-line fragment itself, select it and press `Ctrl+F`.

![Multi-line selection search](https://resources.jetbrains.com/help/img/idea/2025.3/multi_line_selection_search.png)



### Manage your search

IntelliJ IDEA lets you adjust your search process and perform various actions with the displayed search results.

  * The editor automatically scrolls while you type a search query. To disable this behavior, click ![the More button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.moreVertical.svg) and uncheck the Scroll to Results During Typing option.

  * If you want to see the list of previous searches, press `⌥↓` in the search field.

![search history](https://resources.jetbrains.com/help/img/idea/2025.3/search_history.png)
  * If you want to enter a multi-line string, click the ![Enter a new line](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.searchNewLineHover.svg) icon in the search field for a new line.

  * With ![the Regex icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.regex.svg) selected, IntelliJ IDEA automatically escapes special regex symbols with backslash `\` when you search for a text string that contains them.

Keep in mind that if you copy (`Ctrl+C`) the string first and then paste (`Ctrl+V`) it in the search field, the regex symbols will not be taken into account.

For more information about regex, refer to the [search with regex](tutorial-finding-and-replacing-text-using-regular-expressions.html) documentation.

  * Use the ![Previous occurrence](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.up.svg) and ![Next occurrence](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.down.svg) arrows to navigate to the previous or the next occurrence.

  * Work with the list of occurrences `Alt+F7` in the Find tool window, where you have other options, for example, to group your results or to open them in a separate window.

![Found Occurrences in the Find tool window](https://resources.jetbrains.com/help/img/idea/2025.3/find_all_occurrences.png)
  * Click ![the More button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.moreVertical.svg) for Multiple Cursors selection options: to add a selection of the next occurrence (`Alt+J`) or to deselect the previous occurrence (`Alt+Shift+J`).

  * If you want to quickly replace the target of your search in the whole file, press `Ctrl+Alt+Shift+J` and type a new string.

![Replacing all occurrences](https://resources.jetbrains.com/help/img/idea/2025.3/replace_text_in_file.png)
  * You can narrow your search when you click ![the Words icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.inline.exactWords.svg), ![the Match case icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.inline.matchCase.svg) in the search field, or click ![the filter icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.filter.svg) to select a scope for your search.

  * You can press `^⌥X` (previously known as `⌥G`) to quickly toggle ![the Regex icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.regex.svg) the [Regex](regular-expressions.html) option. You can use [regular expressions](tutorial-finding-and-replacing-text-using-regular-expressions.html) to opt for more challenging searches.

  * Press `Ctrl+F7` to see usages of any element in the opened file.

If you don't want IntelliJ IDEA to highlight all found usages in the file, open the Settings dialog (`Ctrl+Alt+S`) and on the Editor | Code Editing page, under the Highlight on Caret Movement section, clear the Usages of element at caret option.

Press `Alt+F7` to [search for usages](find-highlight-usages.html) beyond the current file or `Ctrl+Alt+F7` to open the search results in a separate popup. If you need to configure some options before the search, press `Ctrl+Alt+Shift+F7` to open the Find Usages dialog.




### Replace the search string in a file

  1. Press `Ctrl+R` or select Edit | Find | Replace from the main menu to open the Replace in File window.

  2. In the top field, enter your search string. In the bottom field, enter your replacement string. If you need to preserve the case, click ![the Preserve Case icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.inline.preserveCase.svg) located in the replace field.

![Replace in file pane](https://resources.jetbrains.com/help/img/idea/2025.3/replace_in_file.png)

Click ![Multi-line](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.searchNewLineHover.svg) for a multi-line replace. For example, if you want to replace a comma with a comma and a new line, enter a comma in the search field and a comma and the new line in the replace field.

  3. Click Replace to replace items one by one, Replace all to replace all items in your file, and Exclude to omit some items from replacing.




The options that appear in the Replace window, are similar to the Find window and you can refer to the [manage the search results](#work_with_search_results) section.

07 November 2025

[Bookmarks](bookmarks.html)[Search and replace a target within a project](finding-and-replacing-text-in-project.html)
