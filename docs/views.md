[//]: # (Source: https://www.jetbrains.com/help/idea/views.html)
[//]: # (Downloaded: 2025-12-17 20:06:31)

# Views

A view is a database object that usually represents a database query and can be used as an ordinary table. For more information, refer to your DBMS documentation.

When you double-click a view in the Database tool window (View | Tool Windows | Database), the view is opened in the editor in the Table view. For more information about the views, refer to [View data](tables-view-data.html).

Database table data is available only with the Ultimate subscription. Without the subscription, double-click opens the table DDL definition.

Views ( ![View](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.gutter.dataSchema.svg)) can be found in the Database tool window.

  * For the reference on other node and object icons, refer to the [Data sources and their elements](database-tool-window.html#icons-for-data-sources-and-their-elements) chapter of [Database tool window](database-tool-window.html) topic.

  * Hide, sort, filter, and group tree objects using the tree objects view options in the [View Options](database-tool-window.html#view_options) menu.


![Views in Database](https://resources.jetbrains.com/help/img/idea/2025.3/database_object_view.png)

### Create a view

  1. In the Database tool window, expand the data source tree until the nodes of schemas. 

  2. Right-click the schema node and select New | View.

  3. In the Create dialog that opens, enter the name of your view in the Name field.

  4. In the Source Text pane, enter the statement.

  5. In the Preview pane, you can view and change the generated SQL code.

  6. Click OK to add your view.


![Create a view](https://resources.jetbrains.com/help/img/idea/2025.3/db_create_view.png)

### Modify a view

  1. In the Database tool window, right-click a view and select Navigation | Go to DDL. Alternatively, press `Ctrl+B`.

  2. In the DDL editor that opens, make changes to the source code of your view.

![Modify a view using the DDL editor](https://resources.jetbrains.com/help/img/idea/2025.3/modify_view_ddl_editor.png)
  3. Click the Submit button (![the Submit button](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.submitDB.svg)). Alternatively, press `Ctrl+K`.




### Virtual views

  * If you need to run the same statement and view its result set often, consider using a virtual view which is a IntelliJ IDEA's virtual object. For more information about virtual views, refer to [Virtual views](virtual-views.html). 

![Virtual view](https://resources.jetbrains.com/help/img/idea/2025.3/db_virtual_view.png)



20 November 2025

[Indexes](indexes.html)[Users and roles](database-users-and-roles.html)
