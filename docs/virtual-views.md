[//]: # (Source: https://www.jetbrains.com/help/idea/virtual-views.html)
[//]: # (Downloaded: 2025-12-17 20:06:37)

# Virtual views

If you need to monitor the result set of a certain SQL statement that you run regularly, use a virtual view. Virtual view is an IDE virtual object that lets you have the result set available in the Database tool window. Virtual view is not defined in the database code, its data is not stored in the database, and it cannot be queried with a `SELECT` statement.

For a virtual view, apart from `SELECT` queries, you can also use statements like `show processlist` for MySQL or `exec sp_who2` for Microsoft SQL Server.

For example, to have a list of current database connections for a PostgreSQL database, create a virtual view with the following query:

SELECT * FROM pg_stat_activity; 

The virtual view with the result set of your query will be available in the Database tool window as a virtual object.

![Virtual view](https://resources.jetbrains.com/help/img/idea/2025.3/virtual_view.png)

The SQL statement of virtual view is stored in external-data-<data_source_name>.xml. You can select another name for the XML file and other place to store this file. To change or see the path to the XML document, open data source settings by pressing `Shift+Enter`, click the Options tab and see the Virtual objects and attributes field.

Virtual views ( ![Virtual view](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.virtualView.svg)) can be found in the Database tool window under Database Objects.

  * For the reference on other node and object icons, refer to the [Data sources and their elements](database-tool-window.html#icons-for-data-sources-and-their-elements) chapter of [Database tool window](database-tool-window.html) topic.

  * Hide, sort, filter, and group tree objects using the tree objects view options in the [View Options](database-tool-window.html#view_options) menu.


![Virtual views in Database](https://resources.jetbrains.com/help/img/idea/2025.3/database_object_virtual_view.png)

### Create a virtual view

  1. In the Database tool window, expand the data source tree until the nodes of schemas. 

  2. Right-click the schema node and select New | Virtual View.

  3. In the Create dialog that opens, enter the name of your virtual view in the Name field.

  4. Type your SQL statement in the Query field.

  5. Click OK to add your virtual view.

  6. If the Save external data for <data_source_name> dialog opens, specify the directory for external-data-<data_source_name>.xml file and click Save.


![Create a virtual view](https://resources.jetbrains.com/help/img/idea/2025.3/db_create_virtual_view.png)

28 October 2025

[Virtual foreign keys](virtual-foreign-keys.html)[Virtual columns](virtual-columns.html)
