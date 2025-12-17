[//]: # (Source: https://www.jetbrains.com/help/idea/searching-everywhere.html)
[//]: # (Downloaded: 2025-12-17 20:00:01)

# Search everywhere

You can find any item in the project or outside of it by its name. You can search for files, actions, classes, symbols, settings, UI elements, and anything in Git from a single entry point.

Check the following video for a quick look at how to use this feature:

For more information about searching text within your project, refer to [Search and replace a target within a project](finding-and-replacing-text-in-project.html).

### Search everywhere

  1. In the main menu, go to Navigate | Search Everywhere or press `Shift` twice to open the search window. By default, IntelliJ IDEA displays the list of recent files. 

![search everywhere popup](https://resources.jetbrains.com/help/img/idea/2025.3/search_all_window.png)

Pressing double `Shift` again or `Alt+N` for mnemonics will select the Include non-project items checkbox and the list of search results will extend to external items.

If you switch to other tabs, select the All Places to extend the search results to non-project items.

![the All Places option](https://resources.jetbrains.com/help/img/idea/2025.3/all_places_option.png)
  2. Start typing your query. You can use synonyms in your search. For example, typing `toggle presentation mode` to search for the presentation mode action will display `Enter Presentation Mode` in results.

![Search Everywhere: synonyms](https://resources.jetbrains.com/help/img/idea/2025.3/synonyms_search_everywhere.png)

IntelliJ IDEA lists all the found results where your query is found. Press `Ctrl+Down` to jump to the bottom of the list for `more...` items or `Ctrl+Up` to return to the top of the search results.

Press `Tab` to switch the context of your search to classes, files, symbols, actions, and so on.

You can use the following shortcuts to open the search window with the needed scope right from the start:

     * `Ctrl+N`: finds a class by name.

     * `Ctrl+Shift+N`: finds any file or directory by name (supports _CamelCase_ and _snake_case_). 

If you have a directory or a file that you excluded from your project, IntelliJ IDEA will not include it in the search process.

     * `Ctrl+Alt+Shift+N`: finds a symbol. 

In IntelliJ IDEA, a symbol is any code element such as method, field, class, constant, and so on.

     * `Ctrl+Shift+A`: finds an action by name. You can find any action even if it doesn't have a mapped shortcut or appear in the menu. For example, Emacs actions, such as _kill rings_ , _sticky selection_ , or _hungry backspace_.




To narrow down your search, click the Filter button (![Filter](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.filter.svg)) on the window toolbar and select the appropriate option.

For example, when you search for files, you can exclude some file types from your search.

![Exclude files from search](https://resources.jetbrains.com/help/img/idea/2025.3/exclude_file_type.png)

To see the results of your search in the [Find tool window](find-tool-window.html), click the Open in Find Tool Window button (![the Open in Find tool window icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.openInToolWindow.svg)) on the window toolbar. This button is disabled when you search in the Actions tab.

For more information about viewing recent or edited files, see the [Editor navigation](recent-files-and-changes.html#recent_files) section.

### Search for settings and plugins

You can search for a list of settings, their options, and plugins that you can quickly access, enable, or disable.

  1. Press `Shift` twice to open the search window and type `/`. IntelliJ IDEA lists the available groups of settings.

  2. Select the one you need and press `Enter`.

![Search for Settings](https://resources.jetbrains.com/help/img/idea/2025.3/search_for_settings.png)

As a result, IntelliJ IDEA gives you quick access to the selected setting and its options.

You can also search for plugins and enable or disable them. Type `/plugins` in the search field, in the list of the search results use ON/OFF control keys to enable or disable the needed plugin.

![Search Everywhere: /plugins ](https://resources.jetbrains.com/help/img/idea/2025.3/plugins_search_everywhere.png)

Other tags include `/appearance`, `/system`, `/inspections`, `/registry`, `/intentions`, `/templates`, and `/vcs`.




### Search for URL mappings

IntelliJ IDEA recognizes URLs as symbols. It is supported for Spring, Micronaut, Helidon, JAX-RS and Swagger/OpenAPI. 

  1. Press `Shift` twice to open the search window.

  2. Type `/` and part of the URL mapping you want to search for.

![URL mapping](https://resources.jetbrains.com/help/img/idea/2025.3/url_mappings.png)



### Search for actions

You can search for actions. For example, you can search for a VCS action and access its dialog.

  1. Press `Shift` twice to open the search window.

  2. In the search field, type, for example, `push`. 

![Search for push action](https://resources.jetbrains.com/help/img/idea/2025.3/search_push_action1.png)

IntelliJ IDEA displays the Push action in the Actions section together with the `Ctrl+Shift+K` shortcut, which lets you access the Push dialog.

If the action doesn't have a shortcut, you can assign it without leaving the Search Everywhere window.

![the Search Everywhere window: Pull action](https://resources.jetbrains.com/help/img/idea/2025.3/search_everywhere_pull.png)

After typing the action name in the search field, select it in the search results, press `Alt+Enter` and in the dialog that opens specify a new shortcut.

![the Keyboard shortcut dialog](https://resources.jetbrains.com/help/img/idea/2025.3/pull_action_add_shortcut.png)



### Search for abbreviations

You can assign a short code for the action and use it to search for such action and quickly access it. For example, assign an abbreviation for Color Picker.

  1. In the Settings dialog (`Ctrl+Alt+S`) , go to Keymap. From the options on the right, select Other | Show Color Picker.

  2. From the context menu, select Add abbreviation.

![Color Picker Add Abbreviation](https://resources.jetbrains.com/help/img/idea/2025.3/keymap_color_picker.png)
  3. In the dialog that opens, specify the abbreviation you are going to use, for example, cp and click OK.

  4. Press `Shift` twice to open the search window.

  5. When you type cp in the search field, IntelliJ IDEA will display the item to which you have assigned your abbreviation. Press `Enter` to access the Color Picker dialog.

![Search Results](https://resources.jetbrains.com/help/img/idea/2025.3/search_everywhere_abbreviation_results.png)



### Evaluate mathematical expressions

You can quickly type and evaluate simple mathematical expressions. IntelliJ IDEA also supports HEX, binary, and octal expressions.

  1. Press `Shift` twice to open the search window.

  2. Enter an expression you want to evaluate, IntelliJ IDEA will display the answer in the search results.

![Evaluate expression](https://resources.jetbrains.com/help/img/idea/2025.3/evaluate_expression.png)

You can use basic arithmetic operators — `+`, `-`, `*`, `/`, as well as `^` for power — and basic math functions: `sqrt()`, `sin()`, `cos()`, `tan()`.




### Manage text search in Search Everywhere

The text search is available by default within the Text tab. Within this tab, you can search for text queries, matching words, including case-sensitive scopes, and [regex](tutorial-finding-and-replacing-text-using-regular-expressions.html).

The text search results are also available on the All tab at the bottom of the list. They are displayed when there are few or no other search results available for a given query. You can disable the text search at any time through Advanced Settings.

![Full text search results in Search Everywhere](https://resources.jetbrains.com/help/img/idea/2025.3/ij_se_full_text_search.png)

  1. Press `Ctrl+Alt+S` to open settings and then select Advanced Settings.

  2. Scroll down to the Search Everywhere section and disable Show text search results in Search Everywhere.

  3. Apply the changes and close the dialog.




### Manage tabs for Search Everywhere

You can add more tabs to the Search Everywhere window or disable them through [Advanced Settings](advanced-settings.html).

For example, you can enable the Git tab to search for Git branches or commits. Or, if you have a project with [endpoints](endpoints-tool-window.html), you can enable the Endpoints tab.

  1. Press `Ctrl+Alt+S` to open settings and then select Advanced Settings.

  2. On the Advanced Settings page, in the search field, start typing `Search Everywhere` to see options and tabs that are available. 

![Advanced Settings: Search Everywhere](https://resources.jetbrains.com/help/img/idea/2025.3/search_everywhere_adv_settings.png)
  3. Select the appropriate option and click OK to save the changes.




20 May 2025

[Repair IDE](repair-ide.html)[Write and edit source code](working-with-source-code.html)
