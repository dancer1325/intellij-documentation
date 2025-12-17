[//]: # (Source: https://www.jetbrains.com/help/idea/viewing-query-results.html)
[//]: # (Downloaded: 2025-12-17 20:06:26)

## Display

Usually, when you run a query, you receive results in a table format. IntelliJ IDEA displays the results in a data editor. 

The data editor and viewer, or data editor, provides a user interface for working with data. In the data editor, you can sort, filter, add, edit, and remove the data as well as perform other associated tasks.

By default, IntelliJ IDEA displays the data editor with query results [in a separate tab of the Services tool window](#result_tabs). You can also set the results to appear in your query file by using the [in-editor results feature](#in_editor_results).

### View, format, and work with output

  * For more information about how to view the results, change the output format, and work with data in it, refer to the [Data editor and viewer](data-editor-and-viewer.html) section:

    * [View data](tables-view-data.html)

    * [Compare data](compare-data.html)

    * [Sort data](tables-sort.html)

    * [Filter data](tables-filter.html)

    * [Rows](rows.html)

    * [Cells](cells.html)

![The transposed table viewing mode](https://resources.jetbrains.com/help/img/idea/2025.3/db_viewing_modes_text.png)



For more information about query files and Services tool window, refer to [Query files](query-files.html) and [Services tool window](services-tool-window.html).

### Result tabs in Services tool window

### Run a query and view results in Services tool window

  1. In a query file, type or paste the query that you want to run.

  2. Click ![the Execute button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.run.run.svg) Execute on the toolbar. Alternatively, press `Ctrl+Enter`.




IntelliJ IDEA will display the query result set in the Services tool window tab.

### Open a new tab for each new query

By default, IntelliJ IDEA updates the same tab with results each time you run a new query after the previous one. You can change this behavior and create a tab each time you run a new query.

  1. In the IDE settings `Ctrl+Alt+S`, go to Tools | Database | Query Execution.

  2. Select the Open results in new tab checkbox and click OK.




### Use custom titles for tabs with results

You can define a tab title in the comment section before the query. In the Treat text as title after field, you can reserve a combination of symbols or characters after which any text will be treated as a tab title. By default, no combination is used, so any text after `--` or `/*` is treated as a tab title.

  1. Open settings by pressing `Ctrl+Alt+S`, navigate to Tools | Database | Query Execution | Output and Results.

  2. In the Treat text as title after field, define a combination for tab titles.

To disable this feature, open settings `Ctrl+Alt+S`, navigate to Tools | Database | Query Execution | Output and Results, and clear the Create title for results from comment before query checkbox.

For more examples of custom titles for tabs, refer to [Name the result tabs at youtube.com](https://www.youtube.com/watch?v=U5SOD-eeK50&t=795s).

![Use custom titles for tabs with results](https://resources.jetbrains.com/help/img/idea/2025.3/db_use_custom_titles_for_result_tabs.png)



### Pin the tab with query results

If one and the same tab is used to show your query results, and you get the result that you want to keep, you can pin the tab to the tool window.

  * Right-click the tab and select Pin Tab.

![Pin the result tab](https://resources.jetbrains.com/help/img/idea/2025.3/db_pin_the_result_tab.png)



### In-Editor Results in query files

You can also view the query results within the editor. To do that, use the In-Editor Results feature.

  * To toggle the In-Editor Results feature for the current file, click ![the In-Editor Results icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.editorOutput.svg) In-Editor Results on the toolbar.

![Enable in-editor results for the current file](https://resources.jetbrains.com/help/img/idea/2025.3/db_toggle_in_editor_results_on.png)

![Disable in-editor results for the current file](https://resources.jetbrains.com/help/img/idea/2025.3/db_toggle_in_editor_results_off.png)

  * To toggle the In-Editor Results feature for all files across the IDE, open settings by pressing `Ctrl+Alt+S` and navigate to Database | Query Execution | Output and Results | Results. Select or clear the Show results in editor checkbox.

[![Toggle in-editor results globally](https://resources.jetbrains.com/help/img/idea/2025.3/toggle_in_editor_results_globally.png)](https://resources.jetbrains.com/help/img/idea/2025.3/toggle_in_editor_results_globally.png)


