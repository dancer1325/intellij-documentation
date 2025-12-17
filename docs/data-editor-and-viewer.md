[//]: # (Source: https://www.jetbrains.com/help/idea/data-editor-and-viewer.html)
[//]: # (Downloaded: 2025-12-17 19:23:56)

## Overview

The data editor and viewer, or data editor, provides a user interface for working with data. In the data editor, you can sort, filter, add, edit, and remove the data as well as perform other associated tasks. 

In IntelliJ IDEA, the data editor and viewer lets you work with [database object data](#open_database_object_data), [query result sets](#view_query_result_set), and also [User files data](#view_user_files_data_as_a_table).

![Database object data in data editor](https://resources.jetbrains.com/help/img/idea/2025.3/data_editor_db_object_data_intro.png)

  1. [Toolbar.](#toolbar_controls)

  2. [Filtering](tables-filter.html#filtering_sorting_data) and [sorting](tables-sort.html#filtering_sorting_data) queries pane.

  3. The database object data in a [Table view](tables-view-data.html#data_view_modes_list).




For more information about Database tool window, refer to [Database tool window](database-tool-window.html).

  1. [Toolbar.](#toolbar_controls)

  2. The query result set in a [Table view](tables-view-data.html#data_view_modes_list).




For more information about a Result tab of a Services tool window, refer to [Result tabs](viewing-query-results.html#result_tabs).

  1. [Toolbar.](#toolbar_controls)

  2. The query result set in a [Table view](tables-view-data.html#data_view_modes_list).




For more information about In-Editor Results, refer to [In-Editor Results](viewing-query-results.html#in_editor_results).

![Data editor tab in a delimiter-separated values file editor](https://resources.jetbrains.com/help/img/idea/2025.3/data_editor_for_dsv_files_data.png)

  1. Toolbar.

  2. User file data.




For more information about working with the contents of user files, refer to [Edit DSV files as tables](editing-csv-and-tsv-files.html) and [Data loaders](data-loaders.html).

The default [view mode](tables-view-data.html#data_view_modes) is Table. In this mode, you can [filter](tables-filter.html) and [sort](tables-sort.html) data, edit value of the [cells](cells.html) directly, and work with [rows](rows.html) of the data table.

### Open database object data

To open database object data in data editor, in the Database tool window, do one of the following:

  * Double-click a database object.

  * Select a database object and press `F4`.

  * Select a database object and click ![the Edit Data icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.table.svg) Edit Data on the toolbar.

  * Right-click an object and select Edit Data.


![Data editor tab](https://resources.jetbrains.com/help/img/idea/2025.3/data_editor_db_object_data.png)

### View query result set

To view a query result set in data editor, in a query file, do one of the following:

  * Run an SQL query. The data editor opens in a Result tab of the Services tool window.

  * Click ![the In-Editor Results icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.editorOutput.svg) In-Editor Results on the toolbar and run a query. The data editor opens in the query file in-editor results pane.




For more information about a Result tab of a Services tool window, refer to [Result tabs](viewing-query-results.html#result_tabs).

For more information about In-Editor Results, refer to [In-Editor Results](viewing-query-results.html#in_editor_results).

### View user files data as a table

  * For tabular data user files of [supported formats](data-loaders.html#supported_file_formats), do the following:

    * In the Project tool window, click the tabular data file that you want to view as a table.

For such files, the table view is read-only.

![Contents of an Excel file are displayed in the data editor](https://resources.jetbrains.com/help/img/idea/2025.3/tabular_data_file_data_in_data_editor_excel.png)
  * For DSV user files, do the following:

    1. In the Project tool window, click the DSV file that you want to view and edit as a table.

    2. Right-click inside a delimited text file and then click Edit as Table. Alternatively, you can click the Edit as Table icon in the editor.

    3. In the Configure CSV Format for <file_name> dialog that opens, specify format settings and click OK.

The dialog has three predefined formats (CSV, TSV, and Pipe-separated) and lets you create a custom format. For example, you may require comma-separated values with semicolons as row separators.

Once you confirm the format settings, the Data tab will present data in a table format correspondingly. If you want to use different format settings, repeat the previous procedure and open the data editor again.

If you want to edit only part of the data, select the necessary fragment inside the file.




### Close data editor

  * To close data editor, click ![the Close icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.closeSmall.svg) Close next to the corresponding tab title.



