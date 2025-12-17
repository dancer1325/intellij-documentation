[//]: # (Source: https://www.jetbrains.com/help/idea/tables-sort.html)
[//]: # (Downloaded: 2025-12-17 20:03:52)

# Sort data

To sort column data, click a sorting icon near the column name. By default, a new `ORDER BY` query is sent to the database each time you click a column name. In the Services tool window (Output tab), you can see all the corresponding sorting operations.

Server side sorting is only available for the [database objects data](data-editor-and-viewer.html#open_database_object_data), not for the [query results set](data-editor-and-viewer.html#view_query_result_set).

You can also sort the data on the client side. To do that, click ![the settings icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) Show Options Menu and deselect the Sort via ORDER BY option.

The column sorting is not stacked by default. It means that if you click a sorting icon near the column name to sort data by, the sorting based on other columns will be cleared. If you prefer to use the stacked sorting, click the sorting icon while pressing `Alt`.

State| Description  
---|---  
![No sorting](https://resources.jetbrains.com/help/img/idea/2025.3/db_sorting_marker_default.png)| Indicates that the data is not sorted in this column. The initial state of the sorting marker.  
![Ascending order](https://resources.jetbrains.com/help/img/idea/2025.3/db_sorting_marker_ascending.png)| The data is sorted in the ascending order.  
![Descending order](https://resources.jetbrains.com/help/img/idea/2025.3/db_sorting_marker_descending.png)| The data is sorted in the descending order.  
![Descending order](https://resources.jetbrains.com/help/img/idea/2025.3/db_sorting_marker_level.png)| The number to the right of the marker (1 on the picture) is the sorting level. You can sort by more than one column. In such cases, different columns will have different sorting levels.  
  
To change the default option for stacked sorting, open settings by pressing `Ctrl+Alt+S` and navigate to Tools | Database | Data Editor and Viewer | Data Sorting. Change the value for the Add columns to sorting option.

Also, you can use [the ORDER BY filter](#filtering_sorting_data) and sort data in a table by writing a query in the ORDER BY field.

### Sort table data with a query

If the filter is not available, click the settings icon (![the settings icon ](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg)) and select Show Filter. Alternatively, press `Ctrl+Alt+Shift+F`.

  1. In the ORDER BY field, type your query. The query syntax is the same as in the `ORDER BY` clause but without the keyword.

  2. Press `Enter`.

To reset the filter, click the clear icon (![The clear icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.closeSmall.svg)), or delete the contents of the row filter field and press `Enter`.

To open the filter history, click the arrow icon near the ORDER BY keyword.

![WHERE and ORDER BY fields for sorting](https://resources.jetbrains.com/help/img/idea/2025.3/db_where_and_order_by_fields_for_sorting.png)



### Set default sorting by a primary key

For the tables that have a numeric primary key, IntelliJ IDEA can sort the data by that key. IDE will send a new `ORDER BY` query to the database each time you view the table data in data editor.

  1. Press `Ctrl+Alt+S` to open settings and then select Tools | Database | Data Editor and Viewer. 

  2. Under Data Sorting, select Sort tables by numeric primary key.

  3. Select Ascending or Descending to set the sorting order.

  4. Click OK to save your changes and close the dialog.


![Sort table data by a numeric primary key](https://resources.jetbrains.com/help/img/idea/2025.3/sort_table_data_by_numeric_primary_key.png)

28 October 2025

[Compare the data of database objects](compare-data.html)[Filter data](tables-filter.html)
