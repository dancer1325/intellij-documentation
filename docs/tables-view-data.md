[//]: # (Source: https://www.jetbrains.com/help/idea/tables-view-data.html)
[//]: # (Downloaded: 2025-12-17 20:03:53)

## Data view modes

You can browse and edit data in three modes: Table, Tree, Text, and Transpose. To switch between these modes, click ![the View as button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.show.svg) View as on the toolbar and select the mode that you need.

  * Transpose: viewing mode in which rows and columns are [interchanged](#transposing_table). You can combine this checkbox with other viewing modes.

To make this mode a default for tables and views, open settings by pressing `Ctrl+Alt+S` and navigate to Tools | Database | Data Editor and Viewer. From the Automatically transpose tables list, select Always. When this option is enabled, query results are not transposed.

![The transposed table viewing mode](https://resources.jetbrains.com/help/img/idea/2025.3/db_viewing_modes_transposed_table.png)
  * Table: the default viewing mode of table data. Data in a table is stored in a cell that is an intersection of a vertical column and horizontal row. 

![The table viewing mode](https://resources.jetbrains.com/help/img/idea/2025.3/db_viewing_modes_table.png)
  * Tree: viewing mode in which data is displayed in the key-value table with the possibility to expand the key cell if it contains children nodes. Data from the expanded children node is distributed between key and value columns. You might consider using this mode to work with JSON and array data. 

![The tree viewing mode](https://resources.jetbrains.com/help/img/idea/2025.3/db_viewing_modes_tree.png)
  * Text: viewing mode in which data is displayed as a text. This mode uses data extractors to represent the data. For example, if the CSV data extractor is selected in the Data extractors list on the toolbar, the database object data is displayed in the CSV format.

For more information about data extractors, refer to the [Data extractors](data-extractors.html) topic.

![The transposed table viewing mode](https://resources.jetbrains.com/help/img/idea/2025.3/db_viewing_modes_text.png)



### Transpose a table, a view, or a virtual view

You can rotate the table data from rows to columns and from columns to rows. In the transposed view, the rows and columns are interchanged. You can combine the transpose action with other viewing modes.

  * To transpose a table, a view, or a virtual view, click ![the View as button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.show.svg) View as and select Transpose. 

![The transposed table viewing mode](https://resources.jetbrains.com/help/img/idea/2025.3/db_viewing_modes_transposed_table.png)



### Reload data for the table view

You need to reload data for the table view if you want to synchronize the data that you see in the editor with the contents of the database. Or, when you want to apply the [page size limit](rows.html#making_all_rows_visible_proc) setting after its change.

  * Click ![The Reload Page icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.refresh.svg) Reload Page on the toolbar.

  * Right-click the table and select Reload Page from the context menu.

  * Press `Ctrl+F5`.



