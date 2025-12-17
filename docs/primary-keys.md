[//]: # (Source: https://www.jetbrains.com/help/idea/primary-keys.html)
[//]: # (Downloaded: 2025-12-17 19:51:49)

# Primary keys

A primary key contains unique values and identifies each row in a table.

For some databases, the primary key cannot contain NULL values. A table can have only one primary key, and this primary key can consist of single or multiple columns. When a primary key consists of multiple columns, the data from these columns is used to determine whether a row is unique.

Primary keys ( ![Primary Key](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.goldKey.svg)) can be found in the Database tool window.

  * For the reference on other node and object icons, refer to the [Data sources and their elements](database-tool-window.html#icons-for-data-sources-and-their-elements) chapter of [Database tool window](database-tool-window.html) topic.

  * For the table column icons, refer to the [Possible icon combinations for columns](database-tool-window.html#possible-icon-combinations-for-columns) chapter.

  * Hide, sort, filter, and group tree objects using the tree objects view options in the [View Options](database-tool-window.html#view_options) menu.


![Primary keys in Database](https://resources.jetbrains.com/help/img/idea/2025.3/database_object_primary_key.png)

### Create a primary key

  1. In the Database tool window, expand the data source tree until the nodes of tables. 

  2. Right-click the table node and select New | Primary Key.

  3. In the Modify dialog that opens, enter the name of your primary key in the Name field.

  4. Click the Add button (![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)) in the Columns pane of the primary key editor tab.

  5. In the Column Name field, type or select the column that you want to make a primary key.

  6. In the Preview pane, you can view and change the generated SQL code.

  7. Click OK to add your primary key.


![Create a primary key](https://resources.jetbrains.com/help/img/idea/2025.3/db_create_primary_key.png)

### Create a composite primary key

  1. In the Database tool window, expand the data source tree until the nodes of tables. 

  2. Right-click the table node and select New | Primary Key.

  3. In the Modify dialog that opens, enter the name of your composite primary key in the Name field.

  4. Add the columns that you want to make a primary key of:

     1. Click the Add button (![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)) in the Columns pane of the primary key editor tab.

     2. In the Column Name field, type or select the column that you want to add to the composite primary key.

  5. In the Preview pane, you can view and change the generated SQL code.

  6. Click OK to add your composite primary key.


![Create a composite primary key](https://resources.jetbrains.com/help/img/idea/2025.3/db_create_composite_primary_key.png)

### Make a column a primary key

  1. In the Database tool window, expand the data source tree until the node of a child table.

  2. Right-click a child table and select Modify Table.

  3. In the Modify dialog that opens, select the column that you want to make a primary key.

  4. Click the click the vertical ellipsis icon (![Settings](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moreVertical.svg)) next to the column Name field and select Make Primary Key.

The new primary key will appear under the keys node of the tree. The primary key editing tab will appear next to the column editing one.

  5. Click OK.

![Make a column a primary key](https://resources.jetbrains.com/help/img/idea/2025.3/db_make_primary_key.png)



28 October 2025

[Columns](columns.html)[Foreign keys](foreign-keys.html)
