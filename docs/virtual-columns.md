[//]: # (Source: https://www.jetbrains.com/help/idea/virtual-columns.html)
[//]: # (Downloaded: 2025-12-17 20:06:34)

# Virtual columns

A virtual column is an IDE virtual object that contains values calculated using the data of other columns. It is not defined in the database code, and it cannot be used to create indexes. The data of the virtual column is not stored in the database.

For example, to have a column that would contain data from both `first_name` and `last_name` columns, create a virtual column with the following expression: `first_name || '.' || last_name`.

The virtual column with your expression result will appear in the table, and it will also be available in the Database tool window as a virtual object.

![Virtual column](https://resources.jetbrains.com/help/img/idea/2025.3/virtual_column.png)

The expression used to calculate values for virtual column is stored in external-data-<data_source_name>.xml. You can select another name for the XML file and other place to store this file. To change or see the path to the XML document, open data source settings by pressing `Shift+Enter`, click the Options tab and see the Virtual objects and attributes field.

Virtual columns ( ![Virtual column](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.virtualColumn.svg)) can be found in the Database tool window.

  * For the reference on other node and object icons, refer to the [Data sources and their elements](database-tool-window.html#icons-for-data-sources-and-their-elements) chapter of [Database tool window](database-tool-window.html) topic.

  * For the table column icons, refer to the [Possible icon combinations for columns](database-tool-window.html#possible-icon-combinations-for-columns) chapter.

  * Hide, sort, filter, and group tree objects using the tree objects view options in the [View Options](database-tool-window.html#view_options) menu.


![Virtual columns in Database](https://resources.jetbrains.com/help/img/idea/2025.3/database_object_virtual_column.png)

### Create a virtual column

  1. In the Database tool window, expand the data source tree until the nodes of tables. 

  2. Right-click the table node and select New | Virtual Column.

  3. In the Modify dialog that opens, enter the name of your virtual column in the Name field.

  4. Type your expression in the Expression field.

  5. Click OK to add your virtual column.

  6. If the Save external data for <data_source_name> dialog opens, specify the directory for external-data-<data_source_name>.xml file and click Save.


![Create a virtual column](https://resources.jetbrains.com/help/img/idea/2025.3/db_create_virtual_column.png)

28 October 2025

[Virtual views](virtual-views.html)[Create and Modify dialogs](create-and-modify-dialogs.html)
