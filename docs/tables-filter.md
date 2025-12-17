[//]: # (Source: https://www.jetbrains.com/help/idea/tables-filter.html)
[//]: # (Downloaded: 2025-12-17 20:03:51)

# Filter data

While the Services tool window displays output of your queries, the data editor displays data of a database object as is.

The following topic shows how you can filter data in the data editor. For more information about working with query results in the Services tool window, refer to [Query results](viewing-query-results.html).

In the data editor, you can filter data by using the following approaches:

  * You can use the [local filter](#use_the_local_filter) to filter rows by values in columns.

  * You can specify filtering conditions manually or use [quick filtering options](#using-quick-filtering-options). Quick options are filtering conditions for the current column name. The conditions depend on the value in the current cell.

  * You can filter rows by pressing `Ctrl+F` and [running a search](#filter-rows-when-you-run-a-search) on the table.

  * You can use [the WHERE filter](#filtering_sorting_data) and filter data in a table by writing a query in the WHERE field.




For more information about filtering tables within a schema in Database tool window, see [Speed search in tool windows](speed-search-in-the-tool-windows.html).

### Use the local filter

  1. Click ![the Enable Local Filter icon](https://resources.jetbrains.com/help/img/idea/2025.3/intellij.grid.core.impl.icons.expui.columnFilter.svg) Enable Local Filter on the toolbar to toggle the filters.

  2. In the header of the column, click the ![the Filter icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.filter.svg) filter icon that appears.

  3. To filter the rows by values, either select the values from the list or enter them into the text field.

  4. To filter the rows by values of more columns, click the filter icon and select the values for the other columns.




You can toggle the local filter on and off, IntelliJ IDEA remembers the filtering conditions.

To clear local filters for all columns in your grid, invoke the Find Action popup by pressing `Ctrl+Shift+A`, start typing Clear Local Filter For All Columns, then select the action from the list.

![Clear all local filters using a single action](https://resources.jetbrains.com/help/img/idea/2025.3/db_grid_clear_local_filter.png)

### Use quick filtering options

Server side filtering is only available for the [database objects data](data-editor-and-viewer.html#open_database_object_data), not for the [query results set](data-editor-and-viewer.html#view_query_result_set).

  1. Right-click a cell or multiple cells and navigate to Filter by.

  2. Select an option that you want to apply.

![Using quick filters](https://resources.jetbrains.com/help/img/idea/2025.3/db_tutorial_how_to_find_things_9.png)



### Filter rows when you run a search

  1. Press `Ctrl+F` and select Filter Rows.

  2. Start typing your search query (for example, `John`).

![Quickly find data inside a table without writing a statement](https://resources.jetbrains.com/help/img/idea/2025.3/db_tutorial_how_to_find_things_6.png)



### Filter table data with a query

If the filter is not available, click the settings icon (![the settings icon ](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg)) and select Show Filter. Alternatively, press `Ctrl+Alt+Shift+F`.

  1. In the WHERE field, type your query. The query syntax is the same as in the `WHERE` clause but without the keyword.

  2. Press `Enter`.

To reset the filter, click the clear icon (![The clear icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.closeSmall.svg)), or delete the contents of the row filter field and press `Enter`.

To open the filter history, click the arrow icon near the WHERE keyword.

![WHERE and ORDER BY fields for sorting](https://resources.jetbrains.com/help/img/idea/2025.3/db_where_and_order_by_fields_for_sorting.png)



In the WHERE filter, you can use SQL wildcards within the `LIKE` expressions. For example, the percent sign `%` for zero or more characters and underscore `_` for a single character.

28 October 2025

[Sort data](tables-sort.html)[Rows](rows.html)
